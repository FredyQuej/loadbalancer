FROM httpd:2.4

# Copiamos nuestra configuración personalizada
COPY apache.conf /usr/local/apache2/conf/httpd.conf

# Habilitamos los módulos necesarios (ya están disponibles, solo necesitan ser cargados)
RUN sed -i '/mod_proxy.so/s/^#//g' /usr/local/apache2/conf/httpd.conf && \
    sed -i '/mod_proxy_http.so/s/^#//g' /usr/local/apache2/conf/httpd.conf && \
    sed -i '/mod_proxy_balancer.so/s/^#//g' /usr/local/apache2/conf/httpd.conf && \
    sed -i '/mod_slotmem_shm.so/s/^#//g' /usr/local/apache2/conf/httpd.conf && \
    sed -i '/mod_lbmethod_byrequests.so/s/^#//g' /usr/local/apache2/conf/httpd.conf
