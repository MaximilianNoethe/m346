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

![image](https://github.com/user-attachments/assets/27e4c168-72b9-4f37-926f-2deaf22a8772)


### Web-Server:

Hier haben wir die Performance M ausgewählt auch wenn diese deutlich teurer ist. Dafür haben wir aber genug Speicherplatz wie auch RAM. Lieber geben wir eher mehr Geld aus um unsere Anforderungen zu erreichen anstatt eine schwache Leistung zu haben.

### DB-Server:

Hier haben wir die Standard 2 Version ausgewählt um die nötige Leistung zu erreichen

### Allg. Infos:

Der Load Balancer wie auch die Backups sind automatisch hinzugefügt zu den Versionen, welche wir ausgewählt haben. Die Nachteile dazu sind aber, dass wir z.B. die Backups nicht modifizieren können und somit nicht selber bestimmen wann wir Backups erstellen möchten. Dafür ist es Benutzerfreundliche für Personen, die wenig Ahnung über das Thema haben, weil sie selber nichts konfigurieren müssen und es Heroku für sie es macht.

# 3) Repurchasing
### Zoho CRM
![image](https://github.com/user-attachments/assets/43a6983e-39bb-482b-bee8-f00fa7fea2f5)

### Salesforce
![image](https://github.com/user-attachments/assets/38ef5bea-c17e-4476-88c7-3b22c49e0ea4)

## Entscheidung zwischen Zoho CRM & Salesforce
Zoho CRM
### Erkläung Zoho CRM oder Salesforce
Zoho CRM zeichnet sich durch eine einfache Bedienung aus, ist aber weniger für sehr komplexe Unternehmensstrukturen geeignet. Hingegen erfordert Salesforce aufgrund seinen verschiedenen Funktionen eine längere Lernzeit. Obwohl Zoho nicht die gleiche Flexibilität wie Salesforce hat, ist es viel günstiger und einfacher zu integrieren. Für mittelgroße Unternehmen, wie es in den gegebenen Anforderungen ersichtlich wurde, ist Zoho eine geeignete Lösung.

### Erklärung ob IAAS, PAAS oder SAAS
Ich würde SAAS wählen da es eine günstige, benutzerfreundliche und leicht integrierbare Lösung für mittelgroße Unternehmen bietet. SAAS braucht weniger Wartung und ist schneller einsatzbereit, was den Aufwand für IT-Ressourcen minimiert. Ausserdem ist die Bedienung von SAAS einfacher, wenn man jedoch mehr Erfahrung mit den verschiedenen Service Modellen hat würde ich mich für IAAS entscheiden, weil man dort mehr Einfluss auf die Konfiguration und Anpassung der Infrastruktur hat.

# B) Interpretation der Resultate
### Wie stark unterscheiden sich die Angebote?
Die Angebote unterscheiden sich stark voneinander ab. Mit jedem Service Modell, das man betrachtet, kann man weniger Konfigurationen und Anpassungen an der Infrastruktur vornehmen. Das hat Vor- und Nachteile und wirken sich auf den Preis auf. 

Je mehr Konfigurationen schon vorgegeben sind desto teurer wird es -> IAAS konnte man vieles selber entscheiden somit ist es günstiger aber man muss die passenden Arbeitskräfte dafür haben. SAAS -> Ist hingegen viel teurer, dafür ist vieles schon bereitgestellt und man muss die nötigen Arbeitskräfte dafür nicht haben (Mit Ausnahme von Zoho CRM).

### Welches ist das billigste?
Azure und AWS als IAAS sind die billigsten Optionen.

Zoho CRM ist ein Spezialfall und ziemlich günstig für ein SAAS. Die Erklärung dazu wurde bei "Erkläung Zoho CRM oder Salesforce" erläutert.

### Wieso ist eines davon viel teurer? Ist es aber wirklich teurer?
Das SAAS ist um einiges teurer, weil die Konfigurationen und Anpassungen an den Infrastrukturen schon vorgenommen wurden. Ob es wirklich teurer ist kommt auf die Arbeitskosten und den Aufwand an. Da SaaS die gesamte Konfiguration bereitstellt, muss ein Unternehmen weniger in IT-Ressourcen investieren, um diese Anpassungen selbst vorzunehmen. Dadurch können langfristig höhere Kosten vermieden werden, die durch die  zusätzlicher Arbeitskräfte entstehen würden.


