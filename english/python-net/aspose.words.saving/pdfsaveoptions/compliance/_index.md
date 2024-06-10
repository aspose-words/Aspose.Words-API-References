---
title: PdfSaveOptions.compliance property
linktitle: compliance property
articleTitle: compliance property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.compliance property. Specifies the PDF standards compliance level for output documents."
type: docs
weight: 40
url: /python-net/aspose.words.saving/pdfsaveoptions/compliance/
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
doc = aw.Document(MY_DIR + 'Images.docx')
# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
# Note that some PdfSaveOptions are prohibited when saving to one of the standards and automatically fixed.
# Use IWarningCallback to know which options are automatically fixed.
save_options = aw.saving.PdfSaveOptions()
# Set the "compliance" property to "PdfCompliance.PDF_A1B" to comply with the "PDF/A-1b" standard,
# which aims to preserve the visual appearance of the document as Aspose.Words convert it to PDF.
# Set the "compliance" property to "PdfCompliance.PDF17" to comply with the "1.7" standard.
# Set the "compliance" property to "PdfCompliance.PDF_A1A" to comply with the "PDF/A-1a" standard,
# which complies with "PDF/A-1b" as well as preserving the document structure of the original document.
# Set the "compliance" property to "PdfCompliance.PDF_UA1" to comply with the "PDF/UA-1" (ISO 14289-1) standard,
# which aims to define represent electronic documents in PDF that allow the file to be accessible.
# Set the "Compliance" property to "PdfCompliance.Pdf20" to comply with the "PDF 2.0" (ISO 32000-2) standard.
# Set the "Compliance" property to "PdfCompliance.PdfA4" to comply with the "PDF/A-4" (ISO 19004:2020) standard,
# which preserving document static visual appearance over time.
# This helps with making documents searchable but may significantly increase the size of already large documents.
save_options.compliance = pdf_compliance
doc.save(ARTIFACTS_DIR + 'PdfSaveOptions.compliance.pdf', save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

