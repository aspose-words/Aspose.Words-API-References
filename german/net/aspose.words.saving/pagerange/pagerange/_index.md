---
title: PageRange
linktitle: PageRange
articleTitle: PageRange
second_title: Aspose.Words für .NET
description: Erstellen Sie mühelos individuelle Seitenbereiche mit unserem PageRange-Konstruktor. Verbessern Sie Ihr Dokumentenmanagement mit Präzision und Flexibilität.
type: docs
weight: 10
url: /de/net/aspose.words.saving/pagerange/pagerange/
---
## PageRange constructor

Erstellt ein neues Seitenbereichsobjekt.

```csharp
public PageRange(int from, int to)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| from | Int32 | Der nullbasierte Index der Startseite. |
| to | Int32 | Der nullbasierte Index der letzten Seite. Wenn er den Index der letzten Seite im Dokument überschreitet, wird er beim Rendern gekürzt, damit er in das Dokument passt. |

## Bemerkungen

MaxValue bedeutet die letzte Seite im Dokument.

## Beispiele

Zeigt, wie Seiten basierend auf genauen Seitenbereichen extrahiert werden.

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

### Siehe auch

* class [PageRange](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
