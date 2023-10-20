---
title: OutlineOptions.CreateMissingOutlineLevels
linktitle: CreateMissingOutlineLevels
articleTitle: CreateMissingOutlineLevels
second_title: Aspose.Words für .NET
description: OutlineOptions CreateMissingOutlineLevels eigendom. Ruft einen Wert ab oder legt diesen fest der bestimmt ob fehlende Gliederungsebenen erstellt werden sollen wenn das Dokument exportiert wird in C#.
type: docs
weight: 30
url: /de/net/aspose.words.saving/outlineoptions/createmissingoutlinelevels/
---
## OutlineOptions.CreateMissingOutlineLevels property

Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob fehlende Gliederungsebenen erstellt werden sollen, wenn das Dokument exportiert wird.

Der Standardwert für diese Eigenschaft ist`FALSCH`.

```csharp
public bool CreateMissingOutlineLevels { get; set; }
```

## Beispiele

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

* class [OutlineOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
