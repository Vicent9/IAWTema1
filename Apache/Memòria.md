**Instal·lació del Servidor web Apache**
===

    * Abans de instal·lar el servidor Apache, actualitzarem els paquets del repositori a través del següent comando:

    ![Imatge1](~/projectes/IAWTema1/Apache/Imatges/Captura de 2020-10-13 16-52-12.png)

    * Una vegada actualitzats els paquets, comprovarem si tenim instal·lat el paquet i la seua respectiva versió disponible en els seus repositoris utilitzant el següent comando:

    ![Imatge2](~/projectes/IAWTema1/Apache/Imatges/Captura de 2020-10-13 16-56-38.png)

    Aquest comando ens proporcionarà la informació sobre el paquet instal·lat o versions diferents configurats al sistema.

    * Si no tenim instal·lat el paquet Apache, ho farem amb el comando:

    ![Imatge3](~/projectes/IAWTema1/Apache/Imatges/Captura de 2020-10-13 17-01-10.png)

    * Una vegada finalitzada la instal·lació, podrem accedim al nostre servidor Apache indicant l’adreça local-host a través del comandament «ip a» i després posant-la al navegador corresponent.
      
    ![Imatge4](~/projectes/IAWTema1/Apache/Imatges/Captura de 2020-10-15 12-03-46.png)

    * Per gestionar el servei d’Apache, l’ordre «systemctl» per a: 
        - Aturar el servei
          
        ![Imatge5](~/projectes/IAWTema1/Apache/Imatges/Captura de 2020-10-13 17-25-15.png)
          
          
        - Consultar el estat del servei
          
        ![Imatge6](~/projectes/IAWTema1/Apache/Imatges/Captura de 2020-10-13 17-26-40.png)
 
        - Iniciar el servei
          
        ![Imatge7](~/projectes/IAWTema1/Apache/Imatges/Captura de 2020-10-13 17-26-05.png)
          
        - Reiniciar el servei

        ![Imatge8](~/projectes/IAWTema1/Apache/Imatges/Captura de 2020-10-13 17-27-12.png)

    * A continuació anem a configurar el directori «/var/www/html» on s’ubiquen per defecte les pàgines organitzades en carpetes del servidor.
    En primer lloc per defecte apareixerà com a propietari del directori i del grup root . Per tant canviarem primerament, el grup del propietari de la carpeta «/var/www/html» a «www-data» a través del ordre següent:

    ![Imatge9](~/projectes/IAWTema1/Apache/Imatges/Captura de 2020-10-13 17-43-13.png)

    * Afegirem el nom d’usuari a aquest grup:

    ![Imatge10](~/projectes/IAWTema1/Apache/Imatges/Captura de 2020-10-13 17-46-21.png)

    * A continuació li donarem de forma recursiva per al propietari i al grup i permis de lectura i execució  per als altres i després,activarem el «SetUID» per al grup per a que tot el que creem dins del directori serà propietat també del grup www-data.
    
    ![Imatge11](~/projectes/IAWTema1/Apache/Imatges/Captura de 2020-10-13 17-52-32.png)

    Ademés, ens afegirem com a propietaris d’aquest directori per a treballar amb ell.
      
    ![Imatge12](~/projectes/IAWTema1/Apache/Imatges/Captura de 2020-10-13 17-53-25.png)
      
    * I finalment una vegada establerts els permisos corresponents,podrem treballar dins del directori del contingut web.

    ![Imatge13](~/projectes/IAWTema1/Apache/Imatges/Captura de 2020-10-13 17-58-13.png)
