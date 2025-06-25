# # FROM golang:1.22-alpine AS builder

# # WORKDIR /usr/src/app/

# # # Use Go build cache for dependencies
# # RUN --mount=type=cache,target=/go/pkg/mod \
# #     --mount=type=cache,target=/root/.cache/go-build \
# #     mkdir -p /root/.cache/go-build

# # # Copy
# # COPY go.mod go.sum ./

# # # Download
# # RUN go mod download

# # # Copy the rest of the source code
# # COPY . .

# # RUN go build -o product-catalog .

# # ####################################

# # FROM alpine AS release

# # WORKDIR /usr/src/app/

# # COPY ./products/ ./products/
# # COPY --from=builder /usr/src/app/product-catalog ./product-catalog


# # ENV PRODUCT_CATALOG_PORT 8088
# # ENTRYPOINT [ "./product-catalog" ]


# FROM golang:1.22-alpine AS builder

# WORKDIR /usr/src/app/

# # Use Go build cache for dependencies
# RUN --mount=type=cache,target=/go/pkg/mod \
#     --mount=type=cache,target=/root/.cache/go-build \
#     mkdir -p /root/.cache/go-build

# # Copy go.mod and go.sum to download dependencies
# COPY go.mod go.sum ./

# RUN go mod download

# # Copy the rest of the source code
# COPY . .

# # Build the binary
# RUN go build -o product-catalog .

# ####################################

# FROM alpine AS release

# WORKDIR /usr/src/app/

# # Copy products folder
# COPY ./products/ ./products/

# # Copy the binary from the builder stage
# COPY --from=builder /usr/src/app/product-catalog ./

# # Set environment variable for the port
# ENV PRODUCT_CATALOG_PORT=8088

# # Run the binary
# ENTRYPOINT ["./product-catalog"]


FROM golang:1.22-alpine AS builder

WORKDIR /usr/src/app/

# Use Go build cache for dependencies
RUN --mount=type=cache,target=/go/pkg/mod \
    --mount=type=cache,target=/root/.cache/go-build \
    mkdir -p /root/.cache/go-build

# Copy
COPY go.mod go.sum ./

# Download
RUN go mod download

# Copy the rest of the source code
COPY . .

RUN go build -o product-catalog .

####################################

FROM alpine AS release

WORKDIR /usr/src/app/

COPY ./products/ ./products/
COPY --from=builder /usr/src/app/product-catalog/ ./

ENV PRODUCT_CATALOG_PORT 8088
ENTRYPOINT [ "./product-catalog" ]