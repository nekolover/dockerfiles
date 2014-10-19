#
# Redis Dockerfile
#

# Pull base image.
FROM nekonyuu/archlinux
MAINTAINER Jonathan Raffre <nk@nyuu.eu>

# Update image
ONBUILD RUN pacman -Syyu --noprogressbar --noconfirm

# Install Redis.
RUN \
  pacman -S --noconfirm redis && \
  sed -i 's/^\(bind .*\)$/# \1/' /etc/redis.conf && \
  sed -i 's/^\(daemonize .*\)$/# \1/' /etc/redis.conf && \
  sed -i 's/^\(dir .*\)$/# \1\ndir \/data/' /etc/redis.conf && \
  sed -i 's/^\(logfile .*\)$/# \1/' /etc/redis.conf

# Define mountable directories.
VOLUME ["/data"]

# Define working directory.
WORKDIR /data

# Define default command.
CMD ["redis-server", "/etc/redis.conf"]

# Expose ports.
EXPOSE 6379
