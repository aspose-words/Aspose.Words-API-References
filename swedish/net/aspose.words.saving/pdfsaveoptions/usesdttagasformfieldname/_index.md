---
title: PdfSaveOptions.UseSdtTagAsFormFieldName
linktitle: UseSdtTagAsFormFieldName
articleTitle: UseSdtTagAsFormFieldName
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen PdfSaveOptions UseSdtTagAsFormFieldName förbättrar PDF-formulär genom att använda SDT-kontrolltaggar för bättre organisation och tydlighet.
type: docs
weight: 340
url: /sv/net/aspose.words.saving/pdfsaveoptions/usesdttagasformfieldname/
---
## PdfSaveOptions.UseSdtTagAsFormFieldName property

Anger om SDT-kontrollens tagg eller Id-egenskap ska användas som namn på formulärfältet i PDF.

```csharp
public bool UseSdtTagAsFormFieldName { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk`.

När den är inställd på`falsk`, SDT-kontroll-ID-egenskapen används som namn på formulärfält i PDF.

När den är inställd på`sann`, SDT-kontrollens tagg-egenskap används som namn på formulärfält i PDF.

Om inställd på`sann` och taggen är tom kommer Id-egenskapen att användas som namn på ett formulärfält.

Om inställd på`sann` och taggvärden inte är unika, kommer dubbletter av taggvärden att ändras till unika PDF-formulärfältnamn.

## Exempel

Visar hur man använder SDT-kontrollens tagg eller Id-egenskap som namn på ett formulärfält i PDF.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PreserveFormFields = true;
// När den är satt till 'false' används egenskapen SDT-kontroll-ID som namn på formulärfältet i PDF-filen.
// När den är satt till 'true' används SDT-kontrollens taggegenskap som namn på formulärfältet i PDF-filen.
saveOptions.UseSdtTagAsFormFieldName = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.SdtTagAsFormFieldName.pdf", saveOptions);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
