---
title: PdfSaveOptions.compliance property
linktitle: compliance property
articleTitle: compliance property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.compliance property. Specifies the PDF standards compliance level for output documents."
type: docs
weight: 50
url: /it/python-net/aspose.words.saving/pdfsaveoptions/compliance/
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
# Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo converte il documento in .PDF.
# Nota che alcune PdfSaveOptions sono proibite quando si salva secondo uno degli standard e vengono corrette automaticamente.
# Usa IWarningCallback per sapere quali opzioni sono corrette automaticamente.
save_options = aw.saving.PdfSaveOptions()
# Imposta la proprietà "Compliance" su "PdfCompliance.PdfA1b" per conformarsi allo standard "PDF/A-1b",
# che mira a preservare l'aspetto visivo del documento mentre Aspose.Words lo converte in PDF.
# Imposta la proprietà "Compliance" su "PdfCompliance.Pdf17" per conformarsi allo standard "1.7".
# Imposta la proprietà "Compliance" su "PdfCompliance.PdfA1a" per conformarsi allo standard "PDF/A-1a",
# che è conforme a "PDF/A-1b" oltre a preservare la struttura del documento originale.
# Imposta la proprietà "Compliance" su "PdfCompliance.PdfUa1" per conformarsi allo standard "PDF/UA-1" (ISO 14289-1),
# che mira a definire la rappresentazione di documenti elettronici in PDF che consentono al file di essere accessibile.
# Imposta la proprietà "Compliance" su "PdfCompliance.Pdf20" per conformarsi allo standard "PDF 2.0" (ISO 32000-2).
# Imposta la proprietà "Compliance" su "PdfCompliance.PdfA4" per conformarsi allo standard "PDF/A-4" (ISO 19004:2020),
# che preserva l'aspetto visivo statico del documento nel tempo.
# Imposta la proprietà "Compliance" su "PdfCompliance.PdfA4Ua2" per conformarsi sia a PDF/A-4 (ISO 19005-4:2020)
# e agli standard PDF/UA-2 (ISO 14289-2:2024).
# Imposta la proprietà "Compliance" su "PdfCompliance.PdfUa2" per conformarsi allo standard PDF/UA-2 (ISO 14289-2:2024).
# Questo aiuta a rendere i documenti ricercabili ma può aumentare significativamente le dimensioni di documenti già di grandi dimensioni.
save_options.compliance = pdf_compliance
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.Compliance.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

