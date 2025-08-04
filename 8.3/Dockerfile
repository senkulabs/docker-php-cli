FROM serversideup/php:8.3-cli

# Switch to root so we can do root things
USER root

RUN install-php-extensions bcmath calendar exif intl imagick-stable gd ldap soap

USER www-data
