---
title: PdfSaveOptions.CreateNoteHyperlinks
linktitle: CreateNoteHyperlinks
articleTitle: CreateNoteHyperlinks
second_title: Aspose.Words för .NET
description: Förbättra dina PDF-filer med PdfSaveOptions CreateNoteHyperlinks. Konvertera fotnoter och slutnoter till klickbara länkar för enkel navigering. Standardinställningen är falsk.
type: docs
weight: 60
url: /sv/net/aspose.words.saving/pdfsaveoptions/createnotehyperlinks/
---
## PdfSaveOptions.CreateNoteHyperlinks property

Anger om fotnots-/slutnotsreferenser i huvudtextartikeln ska konverteras till aktiva hyperlänkar. När hyperlänken klickas leder den till motsvarande fotnot/slutnot. Standard är`falsk` .

```csharp
public bool CreateNoteHyperlinks { get; set; }
```

## Exempel

Visar hur man får fotnoter och slutnoter att fungera som hyperlänkar.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Sätt egenskapen "CreateNoteHyperlinks" till "true" för att aktivera alla fotnots-/slutnotssymboler
// i texten fungerar som länkar som, när du klickar, tar oss till deras respektive fotnoter/slutnoter.
// Sätt egenskapen "CreateNoteHyperlinks" till "false" för att inte låta fotnots-/slutnotssymboler länka till någonting.
options.CreateNoteHyperlinks = createNoteHyperlinks;

doc.Save(ArtifactsDir + "PdfSaveOptions.NoteHyperlinks.pdf", options);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
