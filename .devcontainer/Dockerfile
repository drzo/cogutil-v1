# .devcontainer/Dockerfile

FROM opencog/opencog-deps:latest

# Install CMake and Ccache manually
RUN apt-get update && \
    apt-get install -y cmake ccache && \
    rm -rf /var/lib/apt/lists/*

# Set environment variables
ENV CCACHE_DIR=/ws/ccache
ENV MAKEFLAGS=-j2

# Optional: Configure Ccache
RUN ccache --max-size=1G
