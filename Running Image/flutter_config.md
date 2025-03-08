### For Dockerfile

```docker
# Add this file on project root level

# Use a base image with Flutter SDK
FROM cirrusci/flutter:latest

# Set the working directory
WORKDIR /app

# Copy pubspec files and get dependencies
COPY pubspec.yaml pubspec.lock ./
RUN flutter pub get

# Copy the rest of the app
COPY . .

# Build the Flutter app (optional, for web)
RUN flutter build web

# Set the default command
CMD ["flutter", "run"]
```


### .dockerignore
```docker
build/
.android/
.ios/
.flutter-plugins
.flutter-plugins-dependencies
.packages
pubspec.lock
.dart_tool/
```


### Create the image and run container

```docker
# Build the Docker image
docker build -t flutter-app .

# Run the container
docker run -it --rm -p 8080:8080 flutter-app


# If you're using Firebase or any external APIs, ensure you configure environment variables inside Docker.

# Let me know if you need further modifications!

```


```
if another service is running you might need to change it:
docker run -it --rm -p 3000:8080 flutter-app
```
