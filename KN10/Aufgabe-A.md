# 1) Rehosting

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
