Vul onderstaande aan met de antwoorden op de vragen uit de readme.md file. Wil je de oplossingen file van opmaak voorzien? Gebruik dan [deze link](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) om informatie te krijgen over
opmaak met Markdown.


a)
 - De stage "Fetching Source" werd toegevoegd om de source code van de calculator-app uit mijn geforkte GitHub repository op te halen. Hierbij is er gebruik gemaakt van de Jenkins credential manager.

 - Ik heb op mijn terminal dit commando gebruikt om SSH-sleutel te genereren 1)key.pub voor public key en key voor private key: ssh-keygen 

    ![sshkeygen](screenshots/puntA/image1.png)

 - Ik heb gezorgd dat het hostname gedeelte van de sleutel niet mee kopieerde.

    ![sshkeygen](screenshots/puntA/image4.png)

 - In Jenkins heb ik de private sleutel toegevoegd met een ID en mijn github username

    ![credentials](screenshots/puntA/image2.png)
    ![credentials](screenshots/puntA/image3.png)

 - en dan heb ik mijn credential hier gebruikt

    ![credentials](screenshots/puntA/image5.png)

 - In de Jenkinsfile heb ik de stage Fetching Source toegevoegd om de source code van mijn geforkte repository op te halen: 

    ![credentials](screenshots/puntA/image6.png)

 - Hier is mijn console output: 

    ![credentials](screenshots/puntA/image7.png)

---

b)
 - Na de installatie van NodeJs plugin via plugins in manage jenkins heb ik dit toegoevoegd in de Global tool configuration

    ![Nodejs](screenshots/puntB/image1.png)

 - Ik heb ook tools{nodejs 'TINnode-devops'} toegevoegd om de naam van mijn NodeJs installatie te geven dat ik geconfigureerd heb.
 - en Ik heb een stage toegevoegd namelijk Setup NodeJS

    ![Nodejs](screenshots/puntB/image2.png)

 - de console output

    ![Nodejs](screenshots/puntB/image3.png)

---

c)

 - build van Fetching Source

    ![fetching-source](screenshots/puntA/image7.png)

 - build van NodeJS configuration

    ![Nodejs](screenshots/puntB/image3.png)

 - build van installing dependencies

    ![installing-dependencies](screenshots/puntC/image1.png)

 - build van unittest met een rapport gemaakt 

    ![unittest](screenshots/puntC/image2.png)

 - build van Create bundle 

    ![create bundle](screenshots/puntC/image3.png)

 - build van Success, Failure

    ![sucess-en-failure](screenshots/puntC/image4.png)

 - de failed build in de jenkinserrorlog

    ![failed-build](screenshots/puntC/image5.png)

---

d)

 - Automatisch pipeline, elke vrijdag om 14u
    1. Geopend de pipeline configuratie in Jenkins
    2. In de sectie **Triggers** heb ik **Build periodically** ingeschakeld.
    3. Dit cron expressie ingevoerd: **H 14 * * 5**

    ![automatisch-pipeline](screenshots/puntD/image.png)