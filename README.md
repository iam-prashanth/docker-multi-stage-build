# docker-multi-stage-build
Docker multi-stage builds are a feature that allows you to create more efficient Docker images by using multiple build stages within a single Dockerfile. With multi-stage builds, you can separate the build environment from the runtime environment, enabling you to compile and package your application in one stage and then copy the resulting artifacts into a lightweight runtime image in another stage.

Stage 1 (build stage) installs dependencies, copies source code, and builds the application.
Stage 2 uses a lightweight scratch image for the runtime environment. It copies the built artifacts from the build stage and installs only production dependencies. Finally, it specifies the command to run the application.
