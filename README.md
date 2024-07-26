# Software Brauerei - DevOps Challenge

Die Software Brauerei DevOps Challenge für unsere Bewerber. 

## Requirements

1.  Die Aufgabe soll nicht mehr als 2 Stunden in Anspruch nehmen. 
2.  Stelle deine Ergebnisse als Git-Repository (oder mehrere) zur Verfügung.
3.  Die Infrastrukturkosten sollen so gering wie möglich gehalten werden.


## Die Aufgabe
Die Aufgabe besteht aus 3 zusammenhängenden Aufgaben. Ziel ist es, dass dein Repository einfach via `git clone` gecloned und mittels `docker compose up` lokal gestartet werden kann.

### Part I - Die Applikation
Erstelle eine einfach Webapplikation welche über einen HTTP-Endpoint `/saron` den aktuellen SARON Zinssatz von der Webseite der SNB abfragt und als folgenden Json zurück gibt: 
```
GET /saron

content-type: "application/json"
{
    "saron": 1.69
}
``` 

### Part II - Applikation bereitstellen
Erstelle ein Dockerfile um die Applikation zu builden und via `docker compose up` zu starten. Die Applikation muss, über den als Environmentvariable definierten `PORT` erreichbar sein. Ist die Environmentvariable nicht gesezt soll der Port `3000` verwendet werden.

### Part III - Infrastructure
Erstelle die nötige Infrastruktur in [Terraform](https://www.terraform.io/) mit dem [AWS Provider](https://registry.terraform.io/providers/hashicorp/aws/latest/docs). 
#### Zusätzliche Überlegungen
Themen wie Logging, Monitoring und Security sollen auch berücksichtigt werden, jedoch reicht eine Zusammenfassung der dazu gehörenden Gedanken. Dies muss nicht (aber kann) via Terraform umgesetzt werden.

### Zusatzaufgabe
Richte einen GitHub Workflow ein welcher die Infrastruktur via Terraform applied wenn ein Merge auf dem `main` branch erfolgt. Was gilt es dabei zu beachten?