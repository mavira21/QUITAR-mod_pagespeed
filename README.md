El servidor tiene instalado un módulo para generar páginas web de forma rápida pero que puede molestar en fases de desarrollo, para ello desinstalamos el módulo poniendo estos dos comandos en el terminal (putty).  

```sudo nano /opt/bitnami/apache2/conf/httpd.conf```  

Buscar estas dos lineas y poner almohadilla delante, las líneas se encuentran casi al final (ctrl+w pagespeed para buscar).  
Una vez puestas las almohadillas, Ctrl+X y Y para  guardar.  

```#Include conf/pagespeed.conf```  
```#Include conf/pagespeed_libraries.conf```  

Después reiniciar Apache:  

```sudo /opt/bitnami/ctlscript.sh restart apache```
