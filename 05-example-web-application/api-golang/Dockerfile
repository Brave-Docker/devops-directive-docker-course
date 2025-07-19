# Official Go image based on Alpine Linux for minimizing image size
FROM golang:1.21-alpine AS build        

# Set the working directory inside the container
WORKDIR /app

# Create a non-root user to run the application securely
RUN adduser -u 101 -D nonroot

# Copy Go module files and download dependencies
COPY go.mod go.sum ./
RUN --mount=type=cache,target=/go/pkg/mod \
    --mount=type=cache,target=/root/.cache/go-build \
    go mod download

# Copy the rest of the application code
COPY . .

# Disable CGO to ensure a statically linked binary
ENV CGO_ENABLED=0

# Build the Go application. The -tags netgo ensures that the net package uses the pure Go implementation. 
RUN go build \
    #-ldflags="-linkmode external -extldflags -static" \
    -tags netgo \
    -o api-golang

###
FROM scratch

# Set Gin framework to release mode
ENV GIN_MODE=release

# Copy the necessary files from the build stage
COPY --from=build /etc/passwd /etc/passwd
COPY --from=build /app/api-golang /api-golang

# Run the container as a non-root user
USER nonroot

# Expose port 8080 for the application
EXPOSE 8080

# Set the default command to run Go binary
CMD [ "/api-golang" ]







