FROM node:14
ARG SRC_DIR=/opt/i27

RUN mkdir $SRC_DIR
WORKDIR $SRC_DIR
COPY . $SRC_DIR
RUN npm install
EXPOSE 3000
#  Fix: entrypoint.sh is inside .cicd/, so reference it correctly
COPY .cicd/entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
CMD ["/entrypoint.sh"]

























# FROM node:14
# ARG SRC_DIR=/opt/i27

# # Create directory inside the container
# RUN mkdir $SRC_DIR

# # Set the working directory inside the container
# WORKDIR $SRC_DIR

# # Copy the current content to /opt/i27 directory, this is our home directory
# COPY . $SRC_DIR

# # Install Node.js dependencies
# RUN npm install

# # Expose the port
# EXPOSE 3000

# # Copy the entrypoint script
# COPY entrypoint.sh /entrypoint.sh

# # Make the script executable
# RUN chmod +x /entrypoint.sh

# # Use CMD instead of ENTRYPOINT to start the application
# CMD ["/entrypoint.sh"]