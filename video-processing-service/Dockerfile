# Using bun image
FROM oven/bun

# Working directory in the container
WORKDIR /app

# Copy package.json package-lock.json or bun.lockb
COPY package*.json bun.lockb ./

# install ffmpeg in the container
RUN apt-get update && apt-get install -y ffmpeg

# Install any needed package specified in package.json
RUN bun install

# Copy app source inside the docker image
COPY . .

# Make port 3000 availabe outside this container
EXPOSE 3000

CMD [ "bun", "start" ]
