---
title: PageSet Class
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.Saving.PageSet-Klasse für effizientes Dokumentenmanagement. Definieren Sie ganz einfach zufällige Seitensätze und verbessern Sie Ihren Workflow noch heute!
type: docs
weight: 6170
url: /de/net/aspose.words.saving/pageset/
---
## PageSet class

Beschreibt eine zufällige Seitengruppe.

Um mehr zu erfahren, besuchen Sie die[Programmieren mit Dokumenten](https://docs.aspose.com/words/net/programming-with-documents/) Dokumentationsartikel.

```csharp
public sealed class PageSet : IEnumerable<int>
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [PageSet](pageset/#constructor_1)(*int*) | Erstellt einen einseitigen Satz basierend auf dem genauen Seitenindex. |
| [PageSet](pageset/#constructor_2)(*params int[]*) | Erstellt einen Seitensatz basierend auf exakten Seitenindizes. |
| [PageSet](pageset/#constructor)(*params PageRange[]*) | Erstellt einen Seitensatz basierend auf Bereichen. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| static [All](../../aspose.words.saving/pageset/all/) { get; } | Ruft einen Satz mit allen Seiten des Dokuments in ihrer ursprünglichen Reihenfolge ab. |
| static [Even](../../aspose.words.saving/pageset/even/) { get; } | Ruft einen Satz mit allen geraden Seiten des Dokuments in ihrer ursprünglichen Reihenfolge ab. |
| static [Odd](../../aspose.words.saving/pageset/odd/) { get; } | Ruft einen Satz mit allen ungeraden Seiten des Dokuments in ihrer ursprünglichen Reihenfolge ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetEnumerator](../../aspose.words.saving/pageset/getenumerator/)() |  |

## Beispiele

Zeigt, wie eine Seite aus einem Dokument in ein JPEG-Bild gerendert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Erstellen Sie ein "ImageSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um die Art und Weise zu ändern, in der diese Methode das Dokument in ein Bild umwandelt.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
// Setze das "PageSet" auf "1", um die zweite Seite auszuwählen über
// der nullbasierte Index, ab dem mit der Darstellung des Dokuments begonnen werden soll.
options.PageSet = new PageSet(1);

// Wenn wir das Dokument im JPEG-Format speichern, rendert Aspose.Words nur eine Seite.
// Dieses Bild enthält eine Seite ab Seite zwei,
// Dies ist lediglich die zweite Seite des Originaldokuments.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
