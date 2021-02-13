---
title: "GNOME 40: (Wieder) ein neuer Denkansatz"
date: 2021-02-04T08:37:20.899Z
draft: false
image: /images/post/bildschirmfoto-von-2021-02-09-12-38-45.png
description: Mit GNOME 40 stellen die GNOME-Entwickler wie gewohnt wieder mal
  alles auf den Kopf. Welche änderungen die Venutzer zu erwarten haben, klären
  wir hier.
categories:
  - Linux
  - GNOME
  - DE
tags:
  - Linux
  - GNOME
  - DE
  - G40
  - GTK4
  - Fedora33
  - COPR
type: post
post: "true"
---
Der Sprung auf die Version 40 ist längst nicht die einzige wichtige Änderung in der nächsten GNOME-Version. Unter anderem werden die Grundelemente der Benutzeroberfläche grundlegend verändert.

Doch zunächst erstmal zum Namen 3.36, 3.38, 40?

Seit nun fast 10 Jahren folg die Versionierung neuer GNOME-Releases dem Schema *3.XX*.

Die nächste GNOME-Version wird jedoch nicht 3.40 sondern 40 als Versionsnummer mit sich führen.

Dies geschieht unter anderem, um die Versionierung von GNOME und GTK voneinander zu trennen und dem Benutzer einen besseren Überblick über die verschiedenen Versionen zu bieten. Die nächsten Versionen werden ab diesem Jahr als 40.alpha, 40.beta, 40.0, 40.1, 41.alpha … Versioniert.

Dennoch wurden in GNOME 40 viele Änderungen an der Benutzeroberfläche vorgenommen, die wir anschließend näher erläutern, welche dem Versionssprung gerecht werden.

### Die Änderungen in GNOME 40

Die mit GNOME 3 wurde 2011 ein neues Arbeitsflächenkonzept eingeführt. Trotz viel Kritik haben die Entwickler daran festgehalten.

Dennoch versuchen sie kontinuierlich die Benutzererfahrung zu verbessern.

So wurde letztes Jahr entschieden, das bisher vertikale Layout der Aktivitäten-Übersicht gegen ein horizontales Einzutauschen.

Die zukünftigen Änderungen wurden in einem [Artikel](https://blogs.gnome.org/shell-dev/2020/12/18/gnome-shell-ux-plans-for-gnome-40/) am 18. Dezember 2020 im [GNOME Shell Entwicklungsblog](https://blogs.gnome.org/shell-dev/) zum ersten Mal vorgestellt.

Dabei wurden auch folgende Mockups gezeigt:

![Aktivitäten-Übersicht (Mockup)](/images/post/pan-windowpicker-768x478.png "Aktivitäten-Übersicht (Mockup)")

Aktivitäten-Übersicht (Mockup)

![Anwendungsmenü (Mockup)](/images/post/pan-appgrid-768x478.png "Anwendungsmenü (Mockup)")

Anwendungsmen (Mockup)

Bereits jetzt ist die Beta-Version des neuen GNOME Desktops verfügbar, in der die Änderungen zum großen Teil entsprechen den Mockups umgesetzt sind.

![Aktivitäten-Übersicht (40.beta)](/images/post/bildschirmfoto-von-2021-02-13-18-06-14.png "Aktivitäten-Übersicht (40.beta)")

Aktivitäten-Übersicht (40.beta)

![Anwendungsmenü (40.beta)](/images/post/bildschirmfoto-von-2021-02-13-18-06-47.png "Anwendungsmenü (40.beta)")

Anwendungsmenü (40.beta)

Jedoch wurden auch zusätzliche Änderungen eingeführt, wie die Arbeitsflächen-Vorschau über der Aktivitäten-Übersicht.

Schon nach dem Release von GNOME 3.36 wurden in einem [Artikel](https://blogs.gnome.org/shell-dev/2020/04/15/gnome-shell-ux-plans/) die Probleme von GNOME angesprochen. Unter anderem wurde erwähnt, dass der Desktop im Originalzustamd nach dem Start sich eher leer anfühlt und nicht wirklich nützlich ist.

Daher wollen die Entwickler den Benutzern nur einen überflüssigen Schritt ersparen und die Übersicht nun als Startzustand einführen.

Des weiteren gibt es auch kleine kosmetische Änderungen wie das Anzeigen des vollständigen Anwendungsnamen beim darüberwischen mit der Maus:

> ![](/images/post/bildschirmfoto-von-2021-02-13-18-07-50.png)
> ![](/images/post/bildschirmfoto-von-2021-02-13-18-07-57.png)

oder eine Trennlinie zwischen Favoriten und aktiven Apps im Dash:

> ![](/images/post/bildschirmfoto-von-2021-02-13-18-07-26.png)