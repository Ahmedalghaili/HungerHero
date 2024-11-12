# Use a base image with Java 17
FROM openjdk:17-slim

# Install JavaFX dependencies
RUN apt-get update && \
    apt-get install -y openjfx && \
    apt-get clean

# Set the working directory in the container
WORKDIR /app

# Copy the JavaFX project files into the container
COPY . /app

# Compile the JavaFX application
RUN javac -cp /usr/share/openjfx/lib/*:. MainApp.java

# Run the JavaFX application
CMD ["java", "-cp", "/usr/share/openjfx/lib/*:.", "MainApp"]