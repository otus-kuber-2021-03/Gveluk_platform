FROM httpd:2.4
RUN echo 'Hello, World!!!' > /usr/local/apache2/htdocs/homework.html && \
    ln -s /app /usr/local/apache2/htdocs && \
    sed -r 's#^Listen .*#Listen 8000#g' -i /usr/local/apache2/conf/httpd.conf
