# ---- Stage 1: Build the application ----
FROM eclipse-temurin:21-jdk AS builder

WORKDIR /usr/src/app

# Copy Gradle wrapper and config files
COPY gradlew settings.gradle build.gradle ./
COPY gradle ./gradle

# Ensure gradlew is executable
RUN chmod +x gradlew

# Pre-download dependencies
RUN ./gradlew downloadRepos

# Copy the rest of the project files (including src and pb)
COPY . . 

# Optional: move .proto files into expected path
COPY pb ./proto

# Build the distribution
RUN ./gradlew installDist -PprotoSourceDir=./proto

# ---- Stage 2: Runtime image ----
FROM eclipse-temurin:21-jre

WORKDIR /usr/src/app

# Copy built application from builder stage
COPY --from=builder /usr/src/app/build/install/opentelemetry-demo-ad/ ./opentelemetry-demo-ad

ENV AD_PORT=9099

# Run the app
ENTRYPOINT ["./opentelemetry-demo-ad/bin/Ad"]
