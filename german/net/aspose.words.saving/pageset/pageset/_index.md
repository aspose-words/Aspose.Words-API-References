---
title: PageSet.PageSet
second_title: Aspose.Words für .NET-API-Referenz
description: PageSet constructeur. Erstellt ein einseitiges Set basierend auf dem genauen Seitenindex.
type: docs
weight: 10
url: /de/net/aspose.words.saving/pageset/pageset/
---
## PageSet(int) {#constructor_1}

Erstellt ein einseitiges Set basierend auf dem genauen Seitenindex.

```csharp
public PageSet(int page)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| page | Int32 | Nullbasierter Index der Seite. |

### Bemerkungen

Wenn eine Seite gefunden wird, die sich nicht im Dokument befindet, wird während der Wiedergabe eine Ausnahme ausgelöst. MaxValue bedeutet die letzte Seite im Dokument.

### Siehe auch

* class [PageSet](../)
* namensraum [Aspose.Words.Saving](../../pageset/)
* Montage [Aspose.Words](../../../)

---

## PageSet(params int[]) {#constructor_2}

Erstellt ein Seitenset basierend auf exakten Seitenindizes.

```csharp
public PageSet(params int[] pages)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pages | Int32[] | Nullbasierte Indizes von Seiten. |

### Bemerkungen

Wenn eine Seite gefunden wird, die sich nicht im Dokument befindet, wird während der Wiedergabe eine Ausnahme ausgelöst. MaxValue bedeutet die letzte Seite im Dokument.

### Beispiele

Zeigt, wie Seiten basierend auf exakten Seitenindizes extrahiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie dem Dokument fünf Seiten hinzu.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Erstellen Sie ein "XpsSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .XPS konvertiert.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// Verwenden Sie die "PageSet"-Eigenschaft, um einen Satz von Seiten des Dokuments auszuwählen, die in Ausgabe-XPS gespeichert werden sollen.
// In diesem Fall wählen wir über einen nullbasierten Index nur drei Seiten aus: Seite 1, Seite 2 und Seite 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

### Siehe auch

* class [PageSet](../)
* namensraum [Aspose.Words.Saving](../../pageset/)
* Montage [Aspose.Words](../../../)

---

## PageSet(params PageRange[]) {#constructor}

Erstellt ein Seitenset basierend auf Bereichen.

```csharp
public PageSet(params PageRange[] ranges)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| ranges | PageRange[] | Array von Seitenbereichen. |

### Bemerkungen

Wenn ein Bereich gefunden wird, der nach der letzten Seite im Dokument beginnt, wird während der Wiedergabe eine Ausnahme ausgelöst. Alle Bereiche, die nach der letzten Seite enden, werden abgeschnitten, damit sie in das Dokument passen.

### Beispiele

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

* class [PageRange](../../pagerange/)
* class [PageSet](../)
* namensraum [Aspose.Words.Saving](../../pageset/)
* Montage [Aspose.Words](../../../)


