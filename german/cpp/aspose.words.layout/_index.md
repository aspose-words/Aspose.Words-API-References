---
title: "Aspose::Words::Layout Namespace"
linktitle: "Aspose::Words::Layout"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout Namespace. Der Aspose.Words.Layout Namespace stellt Klassen bereit, die den Zugriff auf Informationen ermöglichen, z. B. auf welcher Seite und wo auf einer Seite bestimmte Dokumentelemente positioniert sind, wenn das Dokument in C++ in Seiten formatiert wird."
type: docs
weight: 10000
url: /de/cpp/aspose.words.layout/
---

Der **Aspose.Words.Layout**-Namensraum stellt Klassen bereit, die den Zugriff auf Informationen ermöglichen, wie z. B. auf welcher Seite und wo auf einer Seite bestimmte Dokumentelemente positioniert sind, wenn das Dokument in Seiten formatiert wird.

## Klassen

| Klasse | Beschreibung |
| --- | --- |
| [LayoutCollector](./layoutcollector/) | Diese Klasse ermöglicht die Berechnung von Seitenzahlen von Dokumentknoten. Weitere Informationen finden Sie im Dokumentationsartikel [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [LayoutEnumerator](./layoutenumerator/) | Enumeriert Seitenlayout‑Entitäten eines Dokuments. Sie können diese Klasse verwenden, um das Seitenlayout‑Modell zu durchlaufen. Verfügbare Eigenschaften sind Typ, Geometrie, Text und Seitenindex, an dem die Entität gerendert wird, sowie die Gesamtstruktur und Beziehungen. Verwenden Sie die Kombination von [GetEntity()](../) und [Current](./layoutenumerator/get_current/), um zur Entität zu wechseln, die einem Dokumentknoten entspricht. Weitere Informationen finden Sie im Dokumentationsartikel [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [LayoutOptions](./layoutoptions/) | Enthält die Optionen, die die Steuerung des Dokumentlayout‑Prozesses ermöglichen. Weitere Informationen finden Sie im Dokumentationsartikel [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [PageLayoutCallbackArgs](./pagelayoutcallbackargs/) | Ein Argument, das an [Notify()](./ipagelayoutcallback/notify/) übergeben wird. Weitere Informationen finden Sie im Dokumentationsartikel [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [RevisionOptions](./revisionoptions/) | Ermöglicht die Steuerung, wie Dokumentrevisionen während des Layout‑Prozesses behandelt werden. Weitere Informationen finden Sie im Dokumentationsartikel [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
## Schnittstellen

| Schnittstelle | Beschreibung |
| --- | --- |
| [IPageLayoutCallback](./ipagelayoutcallback/) | Implementieren Sie dieses Interface, wenn Sie Ihre eigene benutzerdefinierte Methode haben möchten, die während des Aufbaus und der Renderung des Seitenlayoutmodells aufgerufen wird. |
## Enums

| Enum | Beschreibung |
| --- | --- |
| [CommentDisplayMode](./commentdisplaymode/) | Gibt den Rendermodus für Dokumentkommentare an. |
| [ContinuousSectionRestart](./continuoussectionrestart/) | Stellt verschiedene Verhaltensweisen beim Berechnen von Seitenzahlen in einem fortlaufenden Abschnitt dar, der die Seitennummerierung neu startet. |
| [LayoutEntityType](./layoutentitytype/) | Typen der Layout-Entitäten. |
| [PageLayoutEvent](./pagelayoutevent/) | Ein Ereigniscodes, der während des Aufbaus und der Renderung des Seitenlayoutmodells ausgelöst wird. Das Seitenlayoutmodell wird in zwei Schritten erstellt. Erstens der "conversion step", dabei zieht das Seitenlayout den Dokumentinhalt und erstellt einen Objektgraphen. Zweitens der "reflow step", dabei werden Strukturen aufgeteilt, zusammengeführt und zu Seiten angeordnet. Abhängig von der Operation, die den Aufbau ausgelöst hat, kann das Seitenlayoutmodell weiter in ein festes Seitenformat gerendert werden oder nicht. Zum Beispiel erfordert das Berechnen der Seitenzahl im Dokument oder das Aktualisieren von Feldern keine Renderung, während der Export nach PDF dies tut. |
| [RevisionColor](./revisioncolor/) | Ermöglicht die Angabe der Farbe von Dokumentrevisionen. |
| [RevisionTextEffect](./revisiontexteffect/) | Ermöglicht die Angabe eines Dekorationseffekts für Revisionen von Dokumenttext. |
| [ShowInBalloons](./showinballoons/) | Gibt an, welche Revisionen in Ballons gerendert werden. |
