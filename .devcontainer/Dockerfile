# Inherit from DOLFINx 0.9.0
FROM dolfinx/dolfinx:v0.9.0

# Set working directory
WORKDIR /root/workspace

# Install system dependencies
RUN apt-get update && apt-get install -y \
    neovim \
    xvfb \
    libgl1 \
    libgl1-mesa-dri \
    && rm -rf /var/lib/apt/lists/*

# Install Python dependencies
RUN /dolfinx-env/bin/python -m pip install --no-cache-dir \
    jupyterlab \
    scipy \
    pyvista

# Disable JupyterLab announcements
RUN jupyter labextension disable "@jupyterlab/apputils-extension:announcements"

# Set default command
CMD ["bash"]
