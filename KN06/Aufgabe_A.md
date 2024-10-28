### Kurze Erklärung in eigenen Worten was ein Reverse Proxy ist:
Ein Reverse Proxy ist ein Server der Anfragen von Nutzern entgegennimmt und an andere Server weiterleitet, der die eigentliche Arbeit macht. Er schützt und verwaltet den Zugriff auf die weiteren Server, die hinter diesem Reverse Proxy sind. Er kann ausserdem Anfragen filtern. So wird der Datenverkehr besser organisiert und die Sicherheit wird erhöht.

### Screenshot von Swagger
![image](https://github.com/user-attachments/assets/bebea65a-6fb2-41c1-9651-ae750a4472f1)

### Screenshot prducts endpoint
![image](https://github.com/user-attachments/assets/45436f89-c634-4583-abe8-e458a758b8cb)

### Screenshot der MongoDB collections
![image](https://github.com/user-attachments/assets/4e696cda-f1a4-4cde-96ed-6bc66297c0ec)

## Schauen Sie sich das Cloud-Init genau an. Welche(r) Teil(e) macht/machen hier überhaupt keinen Sinn in einer produktiven Umgebung?
- Passwortloser sudo-Zugriff für Benutzer "ubuntu":

  ```sudo: ALL=(ALL) NOPASSWD:ALL```

- Aktivierte SSH-Passwortauthentifizierung:

  ```ssh_pwauth: true```

- Unnötige Verwendung von sudo in runcmd.

- Credentials sind öffentlich freigegeben
