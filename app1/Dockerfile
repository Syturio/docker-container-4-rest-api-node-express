#################################################################################
#                                                                               #

#   Documentação Dockerfile: https://docs.docker.com/engine/reference/builder/  #

#   The FROM instruction initializes a new build stage and sets the Base        #
#   Image for subsequent instructions.                                          #
FROM node:alpine

#   The WORKDIR instruction sets the working directory for any RUN, CMD,        #
#   ENTRYPOINT, COPY and ADD instructions that follow it in the Dockerfile.     #
WORKDIR /yolo

#   The COPY instruction copies new files or directories from <src>             #
#   and adds them to the filesystem of the container at the path <dest>.        #
COPY . .

#   The RUN instruction will execute any commands in a new layer on top         #
#   of the current image and commit the results.                                #
#   The resulting committed image will be used for the next step.               #
RUN npm install dependencies
#   Este "dependencies" está no ficheiro "package.json".                        #
#     RUN npm install express --save                                            #  
#     RUN npm install mongoose                                                  #
#     RUN npm install body-parser                                               #
RUN npm install -g nodemon

#   The EXPOSE instruction informs Docker that the container listens            #
#   on the specified network ports at runtime.                                  #
EXPOSE 3000

#   Both CMD and ENTRYPOINT instructions define what command gets executed      #
#   when running a container.                                                   #
#   ENTRYPOINT should be defined when using the container as an executable.     #
CMD ["nodemon", "src/index.js"]

#                                                                               #
#################################################################################
