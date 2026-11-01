# Skull King Online

Ein selbst hostbares Multiplayer-Browser-Kartenspiel mit privaten Räumen (2–8 Personen).

## Lokal starten
1. Node.js 18 oder neuer installieren.
2. Im Projektordner `npm install` ausführen.
3. `npm start` starten.
4. Im Browser `http://localhost:3000` öffnen.

Für Freunde außerhalb Ihres WLANs muss die App auf einem öffentlich erreichbaren Node-Host betrieben werden (z. B. Render oder Railway). Danach teilen Sie die öffentliche Adresse und den fünfstelligen Raumcode.

## Deployment (Render)
- Dieses Projekt in ein privates GitHub-Repository laden.
- Auf Render einen neuen **Web Service** aus dem Repository erstellen.
- Build Command: `npm install`
- Start Command: `npm start`
- Runtime: Node.
- Render setzt `PORT` automatisch.
- Nach dem Deployment die öffentliche HTTPS-Adresse an alle Spieler schicken.

## Enthalten
- Private Räume mit fünfstelligen Codes
- 2–8 Spieler
- Verdeckte Handkarten pro Spieler
- Gleichzeitige Gebotsphase
- Zugreihenfolge und Stichauflösung
- 10 Runden (bei 8 Spielern maximal 8 Karten je Runde)
- Klassische Grundwertung und Kartenboni
- Mobile-freundliche Oberfläche

## Wichtiger Hinweis zum Regelstand
Dies ist ein spielbarer erster Prototyp nach der klassischen Skull-King-Grundwertung. Erweiterungsregeln (Krake, Weißer Wal, Beute), Sondervarianten und einzelne editionsabhängige Details sind nicht enthalten. Vor einer echten Spielrunde sollte die Kartenrangfolge mit der Anleitung eurer Ausgabe abgeglichen werden. Der Code ist ein unabhängiges Fan-Projekt und nicht mit dem Rechteinhaber verbunden.

## Technische Hinweise
- Spielzustand liegt derzeit im Arbeitsspeicher des Servers. Bei einem Serverneustart werden laufende Partien beendet.
- Ein Spieler, der die Verbindung verliert, wird als getrennt markiert; automatische Wiederaufnahme in eine laufende Partie ist noch nicht implementiert.
- Für öffentliche Nutzung sollten Rate-Limits, Wiederverbindung mit Spieler-Token, serverseitige Eingabevalidierung und persistente Räume ergänzt werden.
