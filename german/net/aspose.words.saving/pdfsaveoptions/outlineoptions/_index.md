---
title: PdfSaveOptions.OutlineOptions
second_title: Aspose.Words für .NET-API-Referenz
description: PdfSaveOptions eigendom. Ermöglicht die Angabe von Umrissoptionen.
type: docs
weight: 240
url: /de/net/aspose.words.saving/pdfsaveoptions/outlineoptions/
---
## PdfSaveOptions.OutlineOptions property

Ermöglicht die Angabe von Umrissoptionen.

```csharp
public OutlineOptions OutlineOptions { get; }
```

### Bemerkungen

Aus Überschriften und Lesezeichen können Gliederungen erstellt werden.

Bei Überschriften wird die Gliederungsebene durch die Überschriftenebene bestimmt.

Es ist möglich, die maximale Überschriftenebene festzulegen, die in Gliederungen einbezogen werden soll, oder Überschriftengliederungen überhaupt zu deaktivieren.

Für Lesezeichen kann die Umrissebene in den Optionen als Standardwert für alle Lesezeichen oder als Einzelwerte für bestimmte Lesezeichen festgelegt werden.

Außerdem können Umrisse mit derselben Funktion in das XPS-Format exportiert werden`OutlineOptions` Klasse.

### Beispiele

Zeigt, wie man die Überschriftenebene einschränkt, die in der Gliederung eines gespeicherten PDF-Dokuments angezeigt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Überschriften einfügen, die als Inhaltsverzeichniseinträge der Ebenen 1, 2 und dann 3 dienen können.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.SaveFormat = SaveFormat.Pdf;

// Das ausgegebene PDF-Dokument enthält eine Gliederung, bei der es sich um ein Inhaltsverzeichnis handelt, das die Überschriften im Hauptteil des Dokuments auflistet.
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

// Überschriften einfügen, die als TOC-Einträge der Ebenen 1 und 5 dienen können.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Das ausgegebene PDF-Dokument enthält eine Gliederung, bei der es sich um ein Inhaltsverzeichnis handelt, das die Überschriften im Hauptteil des Dokuments auflistet.
// Durch Klicken auf einen Eintrag in dieser Gliederung gelangen wir zur Position der entsprechenden Überschrift.
// Setzen Sie die Eigenschaft „HeadingsOutlineLevels“ auf „5“, um alle Überschriften der Ebenen 5 und darunter in die Gliederung einzubeziehen.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

// Dieses Dokument enthält Überschriften der Ebenen 1 und 5 und keine Überschriften der Ebenen 2, 3 und 4.
// Das ausgegebene PDF-Dokument behandelt die Gliederungsebenen 2, 3 und 4 als „fehlend“.
// Setzen Sie die Eigenschaft „CreateMissingOutlineLevels“ auf „true“, um alle fehlenden Ebenen in die Gliederung einzubeziehen.
// leere Gliederungseinträge hinterlassen, da keine verwendbaren Überschriften vorhanden sind.
// Setzen Sie die Eigenschaft „CreateMissingOutlineLevels“ auf „false“, um fehlende Gliederungsebenen zu ignorieren.
// und behandeln Sie die Gliederungsüberschriften der Ebene 5 als Ebene 2.
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### Siehe auch

* class [OutlineOptions](../../outlineoptions/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../pdfsaveoptions/)
* Montage [Aspose.Words](../../../)


