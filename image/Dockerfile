FROM quay.io/jupyter/tensorflow-notebook

# Add RUN statements to install packages as the ${NB_USER} defined in the base images.

# Add a "USER root" statement followed by RUN statements
# to install system packages using apt-get, change file permissions, etc.

# If you do switch to root, always be sure to add a "USER ${NB_UID}" command
# at the end of the file to ensure the image runs as a unprivileged user by default.

RUN pip install --no-cache-dir \
    "opencv-python" \
    "opencv-contrib-python" && \
    fix-permissions "${CONDA_DIR}" && \
    fix-permissions "/home/${NB_USER}"
