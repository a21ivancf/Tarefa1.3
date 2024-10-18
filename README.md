# 1.3 Instalación de zonas secundarias

1. Tomaremos a máquina darthsidious, e configuraremola para ser servidor secundario, tanto da zona primaria de resolución directa como de resolución inversa. Captura os ficheiros de configuración en ambalas dúas máquinas. Fai unha captura onde se vexa o reinicio da máquina darthsidious, no que se vexa no log dos dous equipos e que se fixo a transferencia de zona.

   - Configuración do servidor primario
    ![img](Images/ej1.1.png)
   - Configuración do servidor secundaro
    ![img](Images/ej1.2.png)
   - Configuración do compose.yml
    ![img](Images/ej1.3.png)
   - Captura dos logs
    ![img](Images/ej1.4.png)
    ![img](Images/ej1.5.png)

2. Engade un rexistro tipo A (Chewbacca 192.168.20.28) na zona de resolución directa e tamén na de resolución inversa.  Fai unha captura no momento do reinicio do equipo darthvader, no que se vexa o log dos dous equipos e que se amose que se fixo a transferencia de zona. Adxunta tamén unha captura do ficheiro de zona no servidor secundario.
   - Configuración do ficheiro db.starwars.lan
   ![img](Images/ej2.1.png)
   - Configuración do fiecheiro db.20.168.192
   ![img](Images/ej2.2.png)
   - Captura dos logs
   ![img](Images/ej2.3.png)
   ![img](Images/ej2.4.png)
   - Captura dos ficheiros no servidor secundario
   ![img](Images/ej2.5.png)

3. Comproba que o servidor secundario pode resolver ese nome.
   - Captura da resolución do novo rexistro desde o cliente.
   ![img](Images/ej3.png)

4. Fai os cambios necesarios para que as trasferencias se fagan de forma segura empregando chaves.  Repite as capturas e vídeos do punto 2, engadindo o rexistro r2d2 (192.168.20.29)
   - Configuración do ficheiro db.starwars.lan
   ![img](Images/ej4.1.png)
   - Configuración do fiecheiro db.20.168.192
   ![img](Images/ej4.2.png)
   - Configuración do ficherio named.conf.local do servidor primario
   ![img](Images/ej4.3.png)
   - Configuración do ficheiro named.conf.local do servidor secundario
   ![img](Images/ej4.4.png)
   - Captura dos logs
   ![img](Images/ej4.5.png)
   - Captura dos ficheiros no servidor secundario
   ![img](Images/ej4.6.png)
