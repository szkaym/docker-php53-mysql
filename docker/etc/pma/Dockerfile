FROM phpmyadmin/phpmyadmin

# Copy configuration
COPY --chown=root:root etc/pma/config.inc.php /var/www/html/config.inc.php
COPY --chown=root:root etc/pma/sites-enabled/000-default.conf /etc/apache2/sites-enabled/000-default.conf