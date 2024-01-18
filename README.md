# Software Brauerei - DevOps Challenge

Die Software Brauerei DevOps Challenge für unsere Bewerber. 

## Requirements

1.  Die Aufgabe soll nicht mehr als 2 Stunden in Anspruch nehmen. 
2.  Stelle deine Ergebnisse als Git-Repository zur Verfügung.


## Die Aufgabe
Die Aufgabe besteht aus 3 zusammenhängende Aufgaben. Ziel ist es, dass deine Ergebnisse einfach via `git clone` gecloned und mittels `docker compose up` lokal gestartet werden kann.

### Part I - Die Applikation
Erstelle eine einfach Webapplikation welche über einen REST-Endpoint `/saron` den aktuellen SARON Zinssatz von der Webseite der SNB abfragt und als folgenden Json zurück gibt: 
```
GET /saron

content-type: "application/json"
{
    "saron": 1.69
}
``` 

### Part II - Applikation bereitstellen
Erstelle ein Dockerfile welches die Applikation buildet und via `docker compose up` gestartet werden kann. Die Applikation soll auf Port `3000` hören. 

### Part III - Deploy
Das Image soll auf einem k8s Cluster deployed werden. Erstelle die entsprechenden Definition für k8s. 

### Zusatzaufgabe
Wie richtest du eine CI/CD Pipeline ein, welche vom `main` Branch auf Produktion deployed? Hier darfst du Annahmen treffen, bitte entsprechend notieren.