---
title: PdfSaveOptions.OutlineOptions
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die OutlineOptions-Eigenschaft von PdfSaveOptions, um Ihre PDF-Gliederungen mühelos anzupassen. Verbessern Sie die Navigation und die Benutzerfreundlichkeit Ihrer Dokumente!
type: docs
weight: 240
url: /de/net/aspose.words.saving/pdfsaveoptions/outlineoptions/
---
## PdfSaveOptions.OutlineOptions property

Ermöglicht die Angabe von Gliederungsoptionen.

```csharp
public OutlineOptions OutlineOptions { get; }
```

## Bemerkungen

Aus Überschriften und Lesezeichen können Gliederungen erstellt werden.

Bei Überschriften wird die Gliederungsebene durch die Überschriftenebene bestimmt.

Es ist möglich, die maximale Überschriftenebene festzulegen, die in Gliederungen aufgenommen werden soll, oder Überschriftengliederungen vollständig zu deaktivieren.

Für Lesezeichen kann die Gliederungsebene in den Optionen als Standardwert für alle Lesezeichen oder als individueller Wert für bestimmte Lesezeichen festgelegt werden.

Außerdem können Umrisse in das XPS-Format exportiert werden, indem man dasselbe`OutlineOptions` Klasse.

## Beispiele

Zeigt, wie die Überschriftenebene begrenzt wird, die in der Gliederung eines gespeicherten PDF-Dokuments angezeigt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Überschriften einfügen, die als Inhaltsverzeichniseinträge der Ebenen 1, 2 und 3 dienen können.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.SaveFormat = SaveFormat.Pdf;

// Das ausgegebene PDF-Dokument enthält eine Gliederung, d. h. ein Inhaltsverzeichnis, das die Überschriften im Dokumenttext auflistet.
// Durch Klicken auf einen Eintrag in dieser Gliederung gelangen wir zur Position der entsprechenden Überschrift.
// Setzen Sie die Eigenschaft „HeadingsOutlineLevels“ auf „2“, um alle Überschriften, deren Ebenen über 2 liegen, aus der Gliederung auszuschließen.
// Die letzten beiden Überschriften, die wir oben eingefügt haben, werden nicht angezeigt.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
```

Zeigt, wie beim Speichern eines PDF-Dokuments mit Gliederungsebenen gearbeitet wird, die keine entsprechenden Überschriften enthalten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Überschriften einfügen, die als Inhaltsverzeichniseinträge der Ebenen 1 und 5 dienen können.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Das ausgegebene PDF-Dokument enthält eine Gliederung, d. h. ein Inhaltsverzeichnis, das die Überschriften im Dokumenttext auflistet.
// Durch Klicken auf einen Eintrag in dieser Gliederung gelangen wir zur Position der entsprechenden Überschrift.
// Setzen Sie die Eigenschaft „HeadingsOutlineLevels“ auf „5“, um alle Überschriften der Ebenen 5 und darunter in die Gliederung aufzunehmen.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

// Dieses Dokument enthält Überschriften der Ebenen 1 und 5 und keine Überschriften der Ebenen 2, 3 und 4.
// Das PDF-Ausgabedokument behandelt die Gliederungsebenen 2, 3 und 4 als „fehlend“.
// Setzen Sie die Eigenschaft „CreateMissingOutlineLevels“ auf „true“, um alle fehlenden Ebenen in die Gliederung aufzunehmen.
// Gliederungseinträge leer lassen, da keine brauchbaren Überschriften vorhanden sind.
// Setzen Sie die Eigenschaft „CreateMissingOutlineLevels“ auf „false“, um fehlende Gliederungsebenen zu ignorieren.
// und behandeln Sie die Gliederungsüberschriften der Ebene 5 als Überschriften der Ebene 2.
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### Siehe auch

* class [OutlineOptions](../../outlineoptions/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
