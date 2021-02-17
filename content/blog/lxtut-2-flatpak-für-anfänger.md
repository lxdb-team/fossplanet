---
title: Flatpak für Anfänger
date: 2021-02-17T19:06:41.418Z
draft: false
image: /images/post/banner-816x423.png
images:
  - /images/post/banner-816x423.png
description: >-
  Du hast bestimmt schon mal etwas von Flatpak gehört. Wenn du zum Beispiel ein
  Programm für Linux herunterladen möchtest, gibt es auch die Möglichkeit das
  Programm als Flatpak über Flathub zu installieren.

  In diesem Artikel geht es genau um Flatpaks: Wie du Flatpak installierst und einrichtest, sodass du deine gewünschten Anwendungen herunterladen kannst.
categories:
  - Flatpak
  - LXtut
tags:
  - Flatpak
  - Flathub
  - LXtut
type: post
post: true
---
 Du hast bestimmt schon mal etwas von Flatpak gehört. Wenn du zum Beispiel ein Programm für Linux herunterladen möchtest, gibt es auch die Möglichkeit das Programm als Flatpak über *Flathub* zu installieren.\
In diesem Artikel geht es genau um Flatpaks: Wie du Flatpak installierst und einrichtest, sodass du deine gewünschten Anwendungen herunterladen kannst.

### 1. Für wen ist Flatpak überhaupt gedacht?

Flatpak ist vor allem für Entwickler gedacht, die ihre Programme für verschiedenste Linux-Distributionen veröffentlichen möchten. Das spart nämlich eine Menge Arbeit und ist nicht so zeitaufwendig, wie als wenn man für jede einzelne Distribution ein Paket bereitstellt.\
Auf der anderen Seite ist die Flatpak-Technologie auch bei vielen „normalen“ Nutzern beliebt, um die neueste Version eines Paketes installieren zu können. Debian-Nutzer haben beispielsweise damit zu kämpfen, dass nur eine relativ alte (aber dafür stabile) Version eines Paketes in den offiziellen Repositorys verfügbar ist. Genau aus diesem Grund hast du die Möglichkeit, stattdessen (sofern es von dem Entwickler bereitgestellt wird) ein Flatpak zu nutzen.

### 2. Installation

Die Befehle zur Installation von Flatpak für die jeweiligen Linux-Distributionen sind auf der [Flatpak-Website](https://flatpak.org/setup/) verfügbar.

### 3. Einrichtung von Flathub

Bevor du Flatpaks installieren kannst, benötigst du noch deren offizielles Repository namens „Flathub“. Bei Flathub findest du eine Sammlung von verfügbaren Programmen, die du jederzeit installieren kannst.\
Mit folgendem Befehl kannst du Flathub in dein System einbinden:

`flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo`

Anschließend solltest du dein System neu starten, um eventuelle Probleme zu vermeiden.

### 4. Installation eines Flatpaks

Jetzt bist du bereit, die ersten Pakete zu installieren. Um etwas rumzustöbern, kannst du die [offizielle Seite](https://flathub.org) von Flathub im Browser aufrufen, sodass du eine Übersicht aller verfügbaren Flatpaks zum Installieren siehst, und gegebenenfalls nach einem bestimmten Programm suchen kannst.

Wenn du das Passende Programm gefunden hast,
kommst du erstmal auf die Übersichtsseite des Programms.

Als Beispiel nehmen wir jetzt einmal das Open-World-Spiel Minetest.

Es gibt zwei Wege ein Flatpak-Paket zu installieren.

![](/images/post/bildschirmfoto-von-2021-02-08-09-48-41.png)

Falls du die Paketverwaltung GNOME-Software installiert hast, kannst du auf den Installieren-Button klicken. Dann wird eine Datei mit der Endung .flatpakref heruntergeladen, welche ein erweis auf das Flatpak-Paket enthält. Diese kannst du mit GNOME-Software öffnen und installieren.

Des Weiteren können Flatpak-Pakete auch über die Kommandozeile installiert werden.

![](/images/post/bildschirmfoto-von-2021-02-08-09-48-53.png)

Unten auf der Seite findest du den Befehl den du verwenden kannst, falls deine Paketverwaltung keine Flatpaks unterstützt.

Wenn du jedoch nicht den Paketnamen sondern nur den Programmnamen kennst, kannst du ebenfalls das Programm installieren:

`flatpak install flathub minetest`

![](/images/post/terminal-beispiel-flatpak-installation-1024x484.png)

Installation von der Flatpak Version von Minetest, im Terminal.

##### Erklärung des Befehls:

`flatpak`  - Der globale Befehl, womit du Flatpaks verwalten kannst.\
`install`  - Die Option, dass du etwas installieren möchtest.\
`flathub`  - Das Repository, aus dem die Software installiert wird.
`minetest` - Der Name der Anwendung, die du installieren möchtest.

Als Nächstes wirst du gefragt, ob du Minetest nur für dich als User installieren möchtest, oder systemweit. Letztendlich ist es egal, was du auswählst. Wenn du aber „User“ auswählst, und mehrere Benutzer auf deinem Computer eingestellt hast, wird das Flatpak nur auf dem Benutzer verfügbar sein, wo du den Befehl ausführst.\
Wähle also deine gewünschte Option aus.\
Jetzt erscheint in der Kommandozeile, dass ein Flathub namens „minetest“ gefunden wurde, und du wirst gefragt, ob du dieses nutzen möchtest. Dies bestätigst du mit „Y“.\
Bei der nächsten Frage (ob die Runtime für Minetest mit installiert werden soll) solltest du ebenfalls diese bestätigen, weil die Runtime von Minetest benötigt wird.\
Als letzten Schritt, wird dir noch einmal aufgelistet, was alles installiert wird, dies solltest du auch mit „Y“ bestätigen.

**Hinweis:** Die oben beschriebenen Schritte sind nur bei Minetest genauso vorhanden, und können bei jedem anderem Flatpak variieren.

### 5. Weitere nützliche Befehle

`flatpak uninstall <Name>` – Anwendung entfernen\
`flatpak update` – Alle installierten Flatpaks aktualisieren\
`flatpak run <Anwendung>` – Eine Anwendung ausführen\
`flatpak kill <Anwendung>` – Das Beenden einer Anwendung erzwingen (Vorsicht: Kann zu Datenverlust oder ähnlichem führen.)

**Tipp:** Eine Liste mit allen verfügbaren Befehlen siehst du mit dem folgenden Befehl: `man flatpak`

### 6. Fazit

Du siehst also, dass Flatpak bzw. Flathub ein guter Ersatz zu den offiziellen Repositorys darstellt. Die Nutzung von Flatpak stellt in vielen Bereichen Vorteile dar, wie die Stabilität, die weiträumige Kompatibilität unter den Distributionen, sowie natürlich die stets aktuelle Version, für den Nutzer.

Solltest du noch irgendwelche Fragen rund um Flatpak haben, so schreibe diese einfach in die Kommentare dieses Artikels und ich werde versuchen dir zu helfen, denn mögliche Fehlerquellen sind nicht immer auszuschließen.
