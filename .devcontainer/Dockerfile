# Inherit from the official DOLFINx 0.9.0 image
FROM dolfinx/dolfinx:v0.9.0

# Set working directory for Codespace
WORKDIR /root/workspace

# Install system dependencies
RUN apt-get update && apt-get install -y \
    neovim \
    && rm -rf /var/lib/apt/lists/*

# Install Python dependencies to match your requirements
RUN pip install --no-cache-dir \
    jupyterlab==4.0.7 \
    jupyterlab-git==0.50.1

# Disable JupyterLab announcements extension (as in your log)
RUN jupyter labextension disable "@jupyterlab/apputils-extension:announcements"

# Set default command to bash for interactive use
CMD ["bash"]
