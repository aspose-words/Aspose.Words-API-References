---
title: PdfSaveOptions.RenderChoiceFormFieldBorder
linktitle: RenderChoiceFormFieldBorder
articleTitle: RenderChoiceFormFieldBorder
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen PdfSaveOptions RenderChoiceFormFieldBorder förbättrar PDF-formulärets design genom att styra fältgränser för en bättre användarupplevelse.
type: docs
weight: 290
url: /sv/net/aspose.words.saving/pdfsaveoptions/renderchoiceformfieldborder/
---
## PdfSaveOptions.RenderChoiceFormFieldBorder property

Anger om PDF-valformulärets fältkant ska renderas.

```csharp
public bool RenderChoiceFormFieldBorder { get; set; }
```

## Anmärkningar

PDF-valformulärsfält används för export av SDT-kombinationsrutans innehållskontroll, SDT-rullgardinslista Content -kontroll och äldre rullgardinsformulärsfält när[`PreserveFormFields`](../preserveformfields/) alternativet är aktiverat.

Standardvärdet är`sann`.

## Exempel

Visar hur man renderar PDF-fältkanten för valformulär.

```csharp
Document doc = new Document(MyDir + "Legacy drop-down.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PreserveFormFields = true;
saveOptions.RenderChoiceFormFieldBorder = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderChoiceFormFieldBorder.pdf", saveOptions);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
