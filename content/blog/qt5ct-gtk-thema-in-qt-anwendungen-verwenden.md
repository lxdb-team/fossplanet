---
title: "qt5ct: Gtk-Thema in Qt-Anwendungen verwenden"
date: 2021-02-07T10:54:19.335Z
draft: false
image: /images/post/qt5ct.png
description: Wenn du Qt-Anwendungen unter Gtk-Oberflächen wie zum Beispiel Gnome
  oder Xfce installierst, passen diese nicht zum Design der Oberfläche und
  Gtk-Anwendungen. In diesem Artikel zeigen wir eine Lösung für das Problem.
categories:
  - Tutorial
  - LXtut
  - Qt
  - GTK
tags:
  - Tutorial
  - LXtut
  - Qt
  - GTK
  - qt5ct
type: post
post: true
---
Wenn du Qt-Anwendungen unter Gtk-Oberflächen wie zum Beispiel Gnome oder Xfce installierst, passen diese nicht zum Design der Oberfläche und Gtk-Anwendungen.

![](/images/post/qt5ct_1.png)

Doch dieses Problem kann ganz einfach mit einem Programm namens `qt5ct` behoben werden.

### Installation

Um das Werkzeug qt5ct zu verwenden müssen folgende Pakete installiert werden:

> #### Debian / Ubuntu / Linux Mint etc.
>
> `sudo apt install qt5ct qt5-style-plugins`
>
> #### Fedora
>
> `sudo dnf install qt5ct qt5-qtstyleplugins`
>
> #### OpenSUSE
>
> `sudo zypper in qt5ct libqt5-qtstyleplugins-platformtheme-gtk2`

Als nächstes fügst du mit dem folgenden Befehl die Zeile QT_QPA_PLATFORMTHEME=qt5ct in die Datei /etc/environment hinzu:

`echo "QT_QPA_PLATFORMTHEME=qt5ct" | sudo tee -a /etc/environment`

Anschließend musst du deinen PC neu starten.

### Benutzung

Das Programm startest du entweder aus dem Anwendungsmenü, wo es unter Qt5-Einstellungen zu finden ist, oder aus der Konsole mit `/usr/bin/qt5ct` .

![](/images/post/qt5ct-main.png)

Dies ist das Hauptfenster von qt5ct.

Um das Aussehen der Qt-Anwendungen an dies der Gtk-Anwendungen anzulehnen, wählst du im Menü "Stil" das Theme "gtk2" aus.

![](/images/post/qt5ct_2.png)

Als nächstes kannst du noch das Icon-Thema ändern.

Dazu gehst du auf den Tab Symbolthema und wählst das passende Symbolthema aus.

Anschließend klickst du auf „Anwenden“ und dann auf „OK“.

Jetzt sollten die Qt-Anwendungen genau so aussehen, wie die Gtk-Anwendungen.

![](/images/post/page_setup.png)
