FROM serversideup/php:8.3-cli

# Switch to root so we can do root things
USER root

# Install PHP extensions
RUN install-php-extensions bcmath calendar exif intl imagick-stable gd ldap soap

# Install Bun
# Bun's install script needs unzip and curl
RUN apt-get update && \
    apt-get install -y --no-install-recommends curl unzip && \
    rm -rf /var/lib/apt/lists/*

# Install Bun to a system-wide location
ENV BUN_INSTALL=/usr/local
RUN curl -fsSL https://bun.sh/install | bash

# Verify both PHP and Bun are available
RUN php --version && bun --version

USER www-data
