---
title: PdfSaveOptions.OutlineOptions
second_title: Aspose.Words für .NET-API-Referenz
description: PdfSaveOptions eigendom. Ermöglicht das Festlegen von Gliederungsoptionen.
type: docs
weight: 210
url: /de/net/aspose.words.saving/pdfsaveoptions/outlineoptions/
---
## PdfSaveOptions.OutlineOptions property

Ermöglicht das Festlegen von Gliederungsoptionen.

```csharp
public OutlineOptions OutlineOptions { get; }
```

### Bemerkungen

Gliederungen können aus Überschriften und Lesezeichen erstellt werden.

Bei Überschriften wird die Gliederungsebene durch die Überschriftenebene bestimmt.

Es ist möglich, die maximale Überschriftenebene festzulegen, die in Gliederungen aufgenommen werden soll, oder Überschriftengliederungen überhaupt zu deaktivieren.

Für Lesezeichen kann die Gliederungsebene in den Optionen als Standardwert für alle Lesezeichen oder als individuelle Werte für bestimmte Lesezeichen festgelegt werden.

Außerdem können Umrisse in das XPS-Format exportiert werden, indem Sie dasselbe verwenden`OutlineOptions` Klasse.

### Beispiele

Zeigt, wie die Ebene der Überschriften begrenzt wird, die in der Gliederung eines gespeicherten PDF-Dokuments erscheinen.

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

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.SaveFormat = SaveFormat.Pdf;

// Das ausgegebene PDF-Dokument enthält eine Gliederung, die ein Inhaltsverzeichnis ist, das Überschriften im Dokumentkörper auflistet.
// Durch Klicken auf einen Eintrag in dieser Gliederung gelangen wir zur Position der entsprechenden Überschrift.
// Setzen Sie die Eigenschaft "HeadingsOutlineLevels" auf "2", um alle Überschriften, deren Ebenen höher als 2 sind, von der Gliederung auszuschließen.
// Die letzten beiden Überschriften, die wir oben eingefügt haben, werden nicht angezeigt.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
```

Zeigt, wie Sie beim Speichern eines PDF-Dokuments mit Gliederungsebenen arbeiten, die keine entsprechenden Überschriften enthalten.

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

// Das ausgegebene PDF-Dokument enthält eine Gliederung, die ein Inhaltsverzeichnis ist, das Überschriften im Dokumentkörper auflistet.
// Durch Klicken auf einen Eintrag in dieser Gliederung gelangen wir zur Position der entsprechenden Überschrift.
// Setzen Sie die Eigenschaft "HeadingsOutlineLevels" auf "5", um alle Überschriften der Ebenen 5 und darunter in die Gliederung aufzunehmen.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

 // Dieses Dokument enthält Überschriften der Ebenen 1 und 5 und keine Überschriften der Ebenen 2, 3 und 4.
// Das ausgegebene PDF-Dokument behandelt die Gliederungsebenen 2, 3 und 4 als "fehlend".
// Setzen Sie die Eigenschaft "CreateMissingOutlineLevels" auf "true", um alle fehlenden Ebenen in die Gliederung aufzunehmen,
// Leere Gliederungseinträge lassen, da es keine verwendbaren Überschriften gibt.
// Setzen Sie die Eigenschaft "CreateMissingOutlineLevels" auf "false", um fehlende Gliederungsebenen zu ignorieren,
// und behandeln die Überschriften der Gliederungsebene 5 als Ebene 2.
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### Siehe auch

* class [OutlineOptions](../../outlineoptions/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../pdfsaveoptions/)
* Montage [Aspose.Words](../../../)


