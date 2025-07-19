```bash
mkdir go-workspace
export GOPATH=$PWD/go-workspace
go mod download
go run main.go
```

# API Golang Setup
This guide explains how to set up and run the Go API for this project.

## Setup Steps

1. **Create a Go workspace directory:**
   ```bash
   mkdir go-workspace
   ```

2. **Set the GOPATH environment variable:**
   ```bash
   export GOPATH=$PWD/go-workspace
   ```

3. **Download dependencies:**
   ```bash
   go mod download
   ```

4. **Run the application:**
   ```bash
   go run main.go
   ```

The API will now start and run in development mode.