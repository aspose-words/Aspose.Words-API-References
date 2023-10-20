---
title: PdfSaveOptions.CreateNoteHyperlinks
linktitle: CreateNoteHyperlinks
articleTitle: CreateNoteHyperlinks
second_title: Aspose.Words för .NET
description: PdfSaveOptions CreateNoteHyperlinks fast egendom. Anger om fotnots/slutnotsreferenser i huvudtextartikeln ska konverteras till aktiva hyperlänkar. När den klickas leder hyperlänken till motsvarande fotnot/slutnot. Standard ärfalsk  i C#.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/pdfsaveoptions/createnotehyperlinks/
---
## PdfSaveOptions.CreateNoteHyperlinks property

Anger om fotnots-/slutnotsreferenser i huvudtextartikeln ska konverteras till aktiva hyperlänkar. När den klickas leder hyperlänken till motsvarande fotnot/slutnot. Standard är`falsk` .

```csharp
public bool CreateNoteHyperlinks { get; set; }
```

## Exempel

Visar hur man får fotnoter och slutnoter att fungera som hyperlänkar.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Ställ in egenskapen "CreateNoteHyperlinks" till "true" för att ändra alla fotnots-/slutnotssymboler
// i texten fungerar som länkar som vid klick tar oss till deras respektive fotnoter/slutnoter.
// Ställ in egenskapen "CreateNoteHyperlinks" till "false" för att inte ha fotnots-/slutnotssymboler länkade till någonting.
options.CreateNoteHyperlinks = createNoteHyperlinks;

doc.Save(ArtifactsDir + "PdfSaveOptions.NoteHyperlinks.pdf", options);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
