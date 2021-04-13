FROM httpd:2.4
RUN mkdir -p /app && \
    chmod -R 777 /app && \
    mv /usr/local/apache2/htdocs /usr/local/apache2/htdocs_ && \
    ln -s /app /usr/local/apache2/htdocs && \
    echo 'Hello, World!!!' > /usr/local/apache2/htdocs/homework2.html && \
    echo 'Hello, World!!!' > /app/homework.html && \
    #sed -r 's#^DocumentRoot .*#DocumentRoot "/app"#g' -i /usr/local/apache2/conf/httpd.conf && \
    sed -r 's#^Listen .*#Listen 8000#g' -i /usr/local/apache2/conf/httpd.conf
