---
title: PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words für .NET
description: Erstellen Sie mühelos ein maßgeschneidertes einseitiges Set mit dem PageSet-Konstruktor, der für eine präzise Seitenindizierung und ein nahtloses Benutzererlebnis konzipiert ist.
type: docs
weight: 10
url: /de/net/aspose.words.saving/pageset/pageset/
---
## PageSet(*int*) {#constructor_1}

Erstellt einen einseitigen Satz basierend auf dem genauen Seitenindex.

```csharp
public PageSet(int page)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| page | Int32 | Nullbasierter Index der Seite. |

## Bemerkungen

Wenn eine Seite gefunden wird, die nicht im Dokument enthalten ist, wird beim Rendern eine Ausnahme ausgelöst. MaxValue bedeutet die letzte Seite im Dokument.

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

* class [PageSet](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)

---

## PageSet(*params int[]*) {#constructor_2}

Erstellt einen Seitensatz basierend auf exakten Seitenindizes.

```csharp
public PageSet(params int[] pages)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pages | Int32[] | Nullbasierte Indizes von Seiten. |

## Bemerkungen

Wenn eine Seite gefunden wird, die nicht im Dokument enthalten ist, wird beim Rendern eine Ausnahme ausgelöst. MaxValue bedeutet die letzte Seite im Dokument.

## Beispiele

Zeigt, wie Seiten basierend auf genauen Seitenindizes extrahiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//Fügen Sie dem Dokument fünf Seiten hinzu.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Erstellen Sie ein "XpsSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .XPS konvertiert.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// Verwenden Sie die Eigenschaft „PageSet“, um einen Satz von Dokumentseiten auszuwählen, die im XPS-Ausgabeformat gespeichert werden sollen.
// In diesem Fall wählen wir über einen nullbasierten Index nur drei Seiten aus: Seite 1, Seite 2 und Seite 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

### Siehe auch

* class [PageSet](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)

---

## PageSet(*params PageRange[]*) {#constructor}

Erstellt einen Seitensatz basierend auf Bereichen.

```csharp
public PageSet(params PageRange[] ranges)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| ranges | PageRange[] | Array von Seitenbereichen. |

## Bemerkungen

Wenn ein Bereich gefunden wird, der nach der letzten Seite im Dokument beginnt, wird beim Rendern eine Ausnahme ausgelöst. Alle Bereiche, die nach der letzten Seite enden, werden gekürzt, damit sie in das Dokument passen.

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

* class [PageRange](../../pagerange/)
* class [PageSet](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
