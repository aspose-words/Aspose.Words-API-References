---
title: PdfSaveOptions.compliance property
linktitle: compliance property
articleTitle: compliance property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.compliance property. Specifies the PDF standards compliance level for output documents."
type: docs
weight: 50
url: /sv/python-net/aspose.words.saving/pdfsaveoptions/compliance/
---

## PdfSaveOptions.compliance property

Specifies the PDF standards compliance level for output documents.


```python
@property
def compliance(self) -> aspose.words.saving.PdfCompliance:
    ...

@compliance.setter
def compliance(self, value: aspose.words.saving.PdfCompliance):
    ...

```

### Remarks

Default is [PdfCompliance.PDF17](../../pdfcompliance/#PDF17).




### Examples

Shows how to set the PDF standards compliance level of saved PDF documents.

```python
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
# Observera att vissa PdfSaveOptions är förbjudna när man sparar till ett av standarderna och automatiskt korrigeras.
# Använd IWarningCallback för att veta vilka alternativ som automatiskt korrigeras.
save_options = aw.saving.PdfSaveOptions()
# Sätt egenskapen "Compliance" till "PdfCompliance.PdfA1b" för att följa standarden "PDF/A-1b",
# som syftar till att bevara dokumentets visuella utseende när Aspose.Words konverterar det till PDF.
# Sätt egenskapen "Compliance" till "PdfCompliance.Pdf17" för att följa standarden "1.7".
# Ställ in egenskapen "Compliance" till "PdfCompliance.PdfA1a" för att uppfylla standarden "PDF/A-1a",
# som uppfyller "PDF/A-1b" samt bevarar dokumentstrukturen i det ursprungliga dokumentet.
# Ställ in egenskapen "Compliance" till "PdfCompliance.PdfUa1" för att uppfylla standarden "PDF/UA-1" (ISO 14289-1),
# som syftar till att definiera och representera elektroniska dokument i PDF som gör filen tillgänglig.
# Ställ in egenskapen "Compliance" till "PdfCompliance.Pdf20" för att uppfylla standarden "PDF 2.0" (ISO 32000-2).
# Ställ in egenskapen "Compliance" till "PdfCompliance.PdfA4" för att uppfylla standarden "PDF/A-4" (ISO 19004:2020),
# vilket bevarar dokumentets statiska visuella utseende över tid.
# Ställ in egenskapen "Compliance" till "PdfCompliance.PdfA4Ua2" för att uppfylla både PDF/A-4 (ISO 19005-4:2020)
# och PDF/UA-2 (ISO 14289-2:2024) standarderna.
# Ställ in egenskapen "Compliance" till "PdfCompliance.PdfUa2" för att uppfylla standarden PDF/UA-2 (ISO 14289-2:2024).
# Detta hjälper till att göra dokument sökbara men kan avsevärt öka storleken på redan stora dokument.
save_options.compliance = pdf_compliance
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.Compliance.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

