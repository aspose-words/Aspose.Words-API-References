---
title: PdfSaveOptions.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words för .NET
description: PdfSaveOptions Compliance fast egendom. Anger överensstämmelsenivån för PDFstandarder för utdatadokument i C#.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/pdfsaveoptions/compliance/
---
## PdfSaveOptions.Compliance property

Anger överensstämmelsenivån för PDF-standarder för utdatadokument.

```csharp
public PdfCompliance Compliance { get; set; }
```

## Anmärkningar

Standard ärPdf17.

## Exempel

Visar hur du ställer in PDF-standardens överensstämmelsenivå för sparade PDF-dokument.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
// Observera att vissa PdfSaveOptions är förbjudna när du sparar till en av standarderna och automatiskt fixade.
// Använd IWarningCallback för att veta vilka alternativ som automatiskt åtgärdas.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Ställ in egenskapen "Compliance" till "PdfCompliance.PdfA1b" för att följa standarden "PDF/A-1b",
// som syftar till att bevara dokumentets visuella utseende när Aspose.Words konverterar det till PDF.
// Ställ in egenskapen "Compliance" till "PdfCompliance.Pdf17" för att följa standarden "1.7".
// Ställ in egenskapen "Compliance" till "PdfCompliance.PdfA1a" för att följa standarden "PDF/A-1a",
// som överensstämmer med "PDF/A-1b" samt bevarar originaldokumentets dokumentstruktur.
// Ställ in egenskapen "Compliance" till "PdfCompliance.PdfUa1" för att följa standarden "PDF/UA-1" (ISO 14289-1),
// som syftar till att definiera representera elektroniska dokument i PDF som gör att filen är tillgänglig.
// Ställ in egenskapen "Compliance" till "PdfCompliance.Pdf20" för att följa standarden "PDF 2.0" (ISO 32000-2).
// Ställ in egenskapen "Compliance" till "PdfCompliance.PdfA4" för att följa standarden "PDF/A-4" (ISO 19004:2020),
// som bevarar dokumentets statiska visuella utseende över tid.
// Detta hjälper till att göra dokument sökbara men kan avsevärt öka storleken på redan stora dokument.
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### Se även

* enum [PdfCompliance](../../pdfcompliance/)
* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
