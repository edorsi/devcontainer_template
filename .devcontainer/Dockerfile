# CHANGE: Switch from 'bullseye' to 'bookworm' (Debian 12) for better compatibility
FROM mcr.microsoft.com/devcontainers/rust:1-bookworm

# Install generic tools + gRPC/Protobuf compiler
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
    postgresql-client \
    iputils-ping \
    protobuf-compiler \
    libprotobuf-dev

# Install cargo-expand (using --locked to prevent dependency errors)
# Note: Removed cargo-edit as it is largely built-in now
RUN cargo install --locked cargo-expand
