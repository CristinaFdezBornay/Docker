# From an alpine image:
FROM alpine

# Mainteiner:
LABEL maintainer="Cristina Fernandez Bornay"

# Add to the container a text editor:
RUN apk update
RUN apk upgrade
RUN apk add vim

# Launch along with the container:
ENTRYPOINT vim

	# Since we're using ENTRYPOINT, instead of CMD with arguments to the
	# entrypoint, the vim file doen't have a name and we can not save it.
	# We don't really care because the container is removed, but if we wanted
	# to save the file we should change the command to:
	# CMD ["vim", "name_of_the_file"]

# BUILD:
# docker build -t image_ex00 <path>

# RUN:
# docker run --rm -it image_ex00

# CHECK:
# docker ps
# docker exec -it <name container> sh
# apk list | grep Vim
