# Base image: Alpine is a liteweight Linux distribution
FROM python:3.9-alpine

# Set up the working directory
WORKDIR /app

# Install dependencies (separate)
# Do this before the next steps to avoid reinstalling dependencies when rebuilding (Docker caches steps)
COPY ./requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

# After installation: Copy the remaining files into the image
# USE THIS IF YOU NEED TO COPY FILES INTO THE IMAGE
# COPY ./ /app

# Configure the container to run as an executable
# ENTRYPOINT [ "python" ]

# Finally: Run the application
# CMD ["/bin/sh", "-i"]
