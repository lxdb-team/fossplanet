---
title: Release von Firefox 85
date: 2021-01-27T20:08:50.515Z
draft: false
image: /images/post/fx_design_blog_header_1400x770.jpg
description: Mit Firefox 85 stellt Mozilla das erste Firefox-Update im neuen
  Jahr vor. Die Änderungen in der neuen Version werden in diesem Artikel
  vorgestellt.
categories:
  - Firefox
  - Mozilla
  - Browser
tags:
  - Firefox
  - Mozilla
  - Browser
  - Flash
  - Firefox85
  - Ruffle
  - Supercookies
  - Lockwise
  - Proton
type: post
post: "true"
---
Das erste Release von Firefox im Jahr 2021 ist eher klein ausgefallen.

Trotz dessen führt Mozilla mit Firefox 85.0 mehrere wichtige Änderungen ein.

## Die Änderungen in Firefox 85

### Das Ende von Adobe Flash

Die wahrscheinlich wichtigste Änderung ist das Entfernen der Adobe-Flash-Funktionalität.

Letztes Jahr hat Adobe angekündigt, Flash ab 2021 vollständig einzustellen. Unter anderem enthält der Flash Player viele Sicherheitslücken, weswegen schon seit langem empfohlen wird, kein Flash mehr zu nutzen. In Firefox 85 wurde nun der Flash-Code endgültig aus Firefox entfernt.

> Für Nutzer die dennoch Flash brauchen, wurde ein Flash-Emulator namens [Ruffle](https://ruffle.rs/) in der Programmiersprache Rust entwickelt. Doch mehr Informationen dazu wird es in einem separaten Artikel geben.

### Das Isolieren von Supercookies

Supercookies speichern viele Informationen über Nutzer und können nur schwer gelöscht werden. Um jedoch das Tracking über mehrere Websiten hinweg zu vermeiden, versucht Mozilla nun einen neuen Ansatz.

Ab Firefox 85 wird der Website-Cache nun isoliert gespeichert.

Da jede TLD (Top Level Domain) nun einen eigenen Cache besitzt, können die Aktivitäten der Nutzer nun nicht mehr übergreifend verfolgt werden.

### Der verbesserte Lesezeichen-Mechanismus

Das Vorgehen beim Speichern von Lesezeichen hat sich in der neuen Firefox-Version geändert.

* Firefox merkt sich, wo deine Lesezeichen gespeichert werden sollen
* Die Lesezeichenleiste wird in neuen Tabs automatisch angezeigt
* Der Zugriff auf alle Lesezeichen wird durch einen Toolbar-Ordner sichergestellt

### Die Password-Verwaltung

In der integrierten Passwort-Verwaltung Firefox Lockwise wurde ein Button zum Löschen von allen Zugangsdaten hinzugefügt.

### Sicherheitsfixes

In dieser Version wurden viele Sicherheitlücken behoben. Eine Liste ist [hier](https://www.mozilla.org/en-US/security/advisories/mfsa2021-03/) verfügbar.

## Fazit

In der ersten diesjährigen Firefox-Version gibt es keine sehr großen Veränderungen. Trotzdem sorgt Mozilla mit diesem Update für noch mehr Privatsphäre im Internet, weswegen es von jedem installiert werden sollte.

Außerdem arbeitet Mozilla gerade mit Hochdruck an einem neuen Designkonzept, welches mit Firefox 89 voraussichtlich im Mai eingeführt werden soll. Bis dahin werden wir wahrscheinlich keine großen Änderungen in Firefox sehen. Ein Review der ersten Mockups gibt es bald in unserem Blog.