---
title: PdfSaveOptions.CreateNoteHyperlinks
linktitle: CreateNoteHyperlinks
articleTitle: CreateNoteHyperlinks
second_title: Aspose.Words für .NET
description: PdfSaveOptions CreateNoteHyperlinks eigendom. Gibt an ob Fußnoten/Endnotenverweise im Haupttext in aktive Hyperlinks umgewandelt werden. Beim Klicken führt der Hyperlink zur entsprechenden Fußnote/Endnote. Die Standardeinstellung istFALSCH  in C#.
type: docs
weight: 50
url: /de/net/aspose.words.saving/pdfsaveoptions/createnotehyperlinks/
---
## PdfSaveOptions.CreateNoteHyperlinks property

Gibt an, ob Fußnoten-/Endnotenverweise im Haupttext in aktive Hyperlinks umgewandelt werden. Beim Klicken führt der Hyperlink zur entsprechenden Fußnote/Endnote. Die Standardeinstellung ist`FALSCH` .

```csharp
public bool CreateNoteHyperlinks { get; set; }
```

## Beispiele

Zeigt, wie Fußnoten und Endnoten als Hyperlinks fungieren.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „CreateNoteHyperlinks“ auf „true“, um alle Fußnoten-/Endnotensymbole umzuwandeln
// im Text fungieren als Links, die uns beim Anklicken zu den jeweiligen Fußnoten/Endnoten führen.
// Setzen Sie die Eigenschaft „CreateNoteHyperlinks“ auf „false“, damit Fußnoten-/Endnotensymbole nicht mit irgendetwas verknüpft sind.
options.CreateNoteHyperlinks = createNoteHyperlinks;

doc.Save(ArtifactsDir + "PdfSaveOptions.NoteHyperlinks.pdf", options);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
