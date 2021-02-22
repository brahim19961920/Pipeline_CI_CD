# Dockerfile à partir d'une image tomcat8 pour contenir notre application appWebJava
# Pour pouvoir créer cette image on doit executer la commande docker build dans le repertoire contenant le fichier appWeb.war
FROM tomcat:8.0.20-jre8 
COPY webapp.war  /usr/local/tomcat/webapps/webapp.war 

