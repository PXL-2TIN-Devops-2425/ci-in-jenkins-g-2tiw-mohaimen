Vul onderstaande aan met de antwoorden op de vragen uit de readme.md file. Wil je de oplossingen file van opmaak voorzien? Gebruik dan [deze link](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) om informatie te krijgen over
opmaak met Markdown.


a)
- De stage "Fetching Source" werd toegevoegd om de source code van de calculator-app uit mijn geforkte GitHub repository op te halen. Hierbij is er gebruik gemaakt van de Jenkins credential manager.

- Ik heb op mijn terminal dit commando gebruikt om SSH-sleutel te genereren 1)key.pub voor public key en key voor private key: ssh-keygen 

    ![sshkeygen](screenshots/image1.png)

- Ik heb gezorgd dat het hostname gedeelte van de sleutel niet mee kopieerde.

    ![sshkeygen](screenshots/image4.png)

- In Jenkins heb ik de private sleutel toegevoegd met een ID en mijn github username

    ![credentials](screenshots/image2.png)
    ![credentials](screenshots/image3.png)

- en dan heb ik mijn credential hier gebruikt

    ![credentials](screenshots/image5.png)

- In de Jenkinsfile heb ik de stage Fetching Source toegevoegd om de source code van mijn geforkte repository op te halen: 

    ![credentials](screenshots/image6.png)

- Hier is mijn console output: 

    ![credentials](screenshots/image7.png)
b)


c)


d)