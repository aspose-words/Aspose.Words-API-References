---
title: PdfSaveOptions.SaveFormat
second_title: Aspose.Words für .NET-API-Referenz
description: PdfSaveOptions eigendom. Gibt das Format an in dem das Dokument gespeichert wird wenn dieses Speicheroptionsobjekt verwendet wird. Kann nur seinPdf .
type: docs
weight: 280
url: /de/net/aspose.words.saving/pdfsaveoptions/saveformat/
---
## PdfSaveOptions.SaveFormat property

Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann nur seinPdf .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../pdfsaveoptions/)
* Montage [Aspose.Words](../../../)


