# 1) Rehosting

## Azure
![image](https://github.com/user-attachments/assets/4cf3deb2-d55a-4c62-ac65-b6741c88d47f)

### Web-Server:

Wir haben das “App Service” von Azure verwendet

Premium V3 gewählt, weil es mehr Speicher und RAM zur Verfügung stellt. Dank den Einsparungsmöglichkeiten ermöglicht es uns dieses Tarif für nur einen 10Fr. Zuschlag zu verwenden, was besser ist, denn das “Basic” Tarif beinhaltet zu wenig Speicher wie auch RAM.

Wir wählten V2 nicht, weil es dort keine Einsparungsmöglichkeiten gab und somit würde es auf hoher Kosten kommen.

### DB-Server:

Hier wählten wir Azure SQL-Datenbank

Hier haben wir bei den Einsparungsmöglichkeiten ebenfalls die 3 Jahre Reservation ausgewählt und zusätzlich die Azure-Hybridvorteile ausgewählt anstatt die Nutzungsbasierte Bezahlung, weil es in den Hybridvorteilen die notwendigsten Vorgaben enthalten sind und wir keine zusätzlichen brauchen, was nur noch mehr Geld kosten würde. Diese SQL-Lizenz hilft uns nämlich Daten in Azure zu migrieren und zu speichern.

Erklärung warum 3 Jahre Reservationen bei den Einsparungsmöglichkeiten gewählt wurden:

Diese Auswahl erspart uns eine Menge an Geld und somit haben wir diese Server für die nächsten 3 Jahren für unsere Firma reserviert. Das heisst aber, dass wir unseren Ressourcenbedarf voraussehen und im Voraus bezahlen müssen.

Warum Traffic Manager und kein Load Balancer:
Der **Load Balancer** und der **Traffic Manager** in Azure haben unterschiedliche Funktionen und arbeiten auf verschiedenen Ebenen, um den Netzwerkverkehr zu steuern. Aus diesem Grund haben wir den Traffic Manager gewählt, weil wir direkt keinen Load Balancer hinzufügen konnten.

## AWS
![image](https://github.com/user-attachments/assets/c79e43fc-9e3c-4253-8f7f-7db00ca7d4d0)

Wir haben darauf geachtet, dass alle Anforderungen erfüllt werden und gleichzeitig die monatlichen Kosten möglichst niedrig bleiben.

Für den Webserver haben wir die Instanz g4d.small ausgewählt, da sie exakt den geforderten Spezifikationen entspricht (1 Core, 2 GB RAM).

Den Datenbankserver haben wir mit der Instanz g4d.medium konfiguriert, da diese ebenfalls die Anforderungen erfüllt (2 Cores, 100 GB Speicher, 4 GB RAM).

Die täglichen Backups stellen den kostenintensivsten Teil dar, da jeden Tag 100 GB gesichert werden, was in einer Woche 700 GB und im Monat mindestens 28 Sicherungen ergibt.

Im Gegensatz dazu sind die wöchentlichen und monatlichen Backups deutlich günstiger, da sie seltener durchgeführt werden und somit weniger Speicher benötigt wird.

# 2) Replatforming
![image](https://github.com/user-attachments/assets/10891f4e-4662-453d-a898-a77107f58a69)

### Web-Server:

Hier haben wir die Performance M ausgewählt auch wenn diese deutlich teurer ist. Dafür haben wir aber genug Speicherplatz wie auch RAM. Lieber geben wir eher mehr Geld aus um unsere Anforderungen zu erreichen anstatt eine schwache Leistung zu haben.

### DB-Server:

Hier haben wir die Standard 2 Version ausgewählt um die nötige Leistung zu erreichen

### Allg. Infos:

Der Load Balancer wie auch die Backups sind automatisch hinzugefügt zu den Versionen, welche wir ausgewählt haben. Die Nachteile dazu sind aber, dass wir z.B. die Backups nicht modifizieren können und somit nicht selber bestimmen wann wir Backups erstellen möchten. Dafür ist es Benutzerfreundliche für Personen, die wenig Ahnung über das Thema haben, weil sie selber nichts konfigurieren müssen und es Heroku für sie es macht.

