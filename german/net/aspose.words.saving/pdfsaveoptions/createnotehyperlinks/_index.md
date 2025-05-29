---
title: PdfSaveOptions.CreateNoteHyperlinks
linktitle: CreateNoteHyperlinks
articleTitle: CreateNoteHyperlinks
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre PDFs mit den CreateNoteHyperlinks von PdfSaveOptions. Wandeln Sie Fußnoten und Endnoten in anklickbare Links um, um die Navigation zu vereinfachen. Standard: „false“.
type: docs
weight: 60
url: /de/net/aspose.words.saving/pdfsaveoptions/createnotehyperlinks/
---
## PdfSaveOptions.CreateNoteHyperlinks property

Gibt an, ob Fußnoten-/Endnotenverweise im Haupttext in aktive Hyperlinks umgewandelt werden sollen. Beim Anklicken führt der Hyperlink zur entsprechenden Fußnote/Endnote. Standard ist`FALSCH` .

```csharp
public bool CreateNoteHyperlinks { get; set; }
```

## Beispiele

Zeigt, wie Fußnoten und Endnoten als Hyperlinks fungieren.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft "CreateNoteHyperlinks" auf "true", um alle Fußnoten-/Endnotensymbole zu aktivieren
// im Text fungieren als Links, die uns beim Anklicken zu den jeweiligen Fußnoten/Endnoten führen.
// Setzen Sie die Eigenschaft „CreateNoteHyperlinks“ auf „false“, damit Fußnoten-/Endnotensymbole auf nichts verlinken.
options.CreateNoteHyperlinks = createNoteHyperlinks;

doc.Save(ArtifactsDir + "PdfSaveOptions.NoteHyperlinks.pdf", options);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
