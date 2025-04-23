# Inherit from the official DOLFINx 0.9.0 image
FROM dolfinx/dolfinx:v0.9.0

# Set working directory
WORKDIR /root/workspace

# Install additional dependencies (optional, add as needed)
RUN apt-get update && apt-get install -y \
    git \
    nano \
    && rm -rf /var/lib/apt/lists/*

# Install Python packages (optional, add as needed)
RUN pip install --no-cache-dir \
    matplotlib \
    scipy \
    jupyterlab 

USER vscode

# Copy your code into the container (optional, can be mounted instead)
# COPY navier_stokes_dolfinx.py .

# Set default command to bash for interactive use
CMD ["bash"]
