---
title: Release von Firefox 85
date: 2021-01-27T11:49:06.265Z
draft: false
image: /images/post/fx_design_blog_header_1400x770.jpg
description: ""
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
type: post
post: "true"
---
Das erste Release von Firefox im Jahr 2021 ist eher klein ausgefallen.

Trotz dessen führt Mozilla mit Firefox 85 mehrere wichtige Änderungen ein.

## Änderungen in Firefox 85

### Das Ende von Adobe Flash

Die wahrscheinlich wichtigste Änderung ist das Entfernen der Adobe Flash-Funktionalität.

Letztes Jahr hat Adobe angekündigt, Flash ab 2021 vollständig einzustellen. Unter anderem enthält der Flash Player viele SIcherheitslücken, weswegen schon seit langem empfohlen wird, kein Flash mehr zu nutzen. In Firefox 85 wurde nun der Flash-Code endgültig aus Firefox entfernt.

> Für Nutzer die dennoch Flash brauchen, wurde ein Flash-Emulator namens [Ruffle](https://ruffle.rs/) in der Programmiersprache Rust entwickelt. Doch mehr Informationen dazu wird es in einem separaten Artikel geben.

### Isolieren von Supercookies

Superkookies speichern viele Informationen über nutzer und können nur schwer gelöscht werden. Um jedoch das Tracking über mehrere Websiten hinweg zu vermeiden, versucht Mozilla nun einen neuen Ansatz.

Ab Firefox 85 wird der Website-Cache nun isoliert gespeichert.

Da jede TLD (Top Level Domain) nun einen eigenen Cache besitzt, können die Aktivitäten der Nutzer nun nicht mehr übergreifend verfolgt werden.

### Verbesserter Lesezeichen-Mechanismus

Das Vorgehen beim Speichern von Lesezeichen hat sich in der neuen Firefox-Version geändert.