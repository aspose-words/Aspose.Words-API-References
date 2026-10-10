---
title: PdfSaveOptions.compliance property
linktitle: compliance property
articleTitle: compliance property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.compliance property. Specifies the PDF standards compliance level for output documents."
type: docs
weight: 50
url: /es/python-net/aspose.words.saving/pdfsaveoptions/compliance/
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
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
# Tenga en cuenta que algunas PdfSaveOptions están prohibidas al guardar según uno de los estándares y se corrigen automáticamente.
# Utilice IWarningCallback para saber qué opciones se corrigen automáticamente.
save_options = aw.saving.PdfSaveOptions()
# Establezca la propiedad "Compliance" a "PdfCompliance.PdfA1b" para cumplir con el estándar "PDF/A-1b",
# que tiene como objetivo preservar la apariencia visual del documento mientras Aspose.Words lo convierte a PDF.
# Establezca la propiedad "Compliance" a "PdfCompliance.Pdf17" para cumplir con el estándar "1.7".
# Establezca la propiedad "Compliance" a "PdfCompliance.PdfA1a" para cumplir con el estándar "PDF/A-1a",
# que cumple con "PDF/A-1b" además de preservar la estructura del documento original.
# Establezca la propiedad "Compliance" a "PdfCompliance.PdfUa1" para cumplir con el estándar "PDF/UA-1" (ISO 14289-1),
# que tiene como objetivo definir la representación de documentos electrónicos en PDF que permitan que el archivo sea accesible.
# Establezca la propiedad "Compliance" a "PdfCompliance.Pdf20" para cumplir con el estándar "PDF 2.0" (ISO 32000-2).
# Establezca la propiedad "Compliance" a "PdfCompliance.PdfA4" para cumplir con el estándar "PDF/A-4" (ISO 19004:2020),
# que preserva la apariencia visual estática del documento a lo largo del tiempo.
# Establezca la propiedad "Compliance" a "PdfCompliance.PdfA4Ua2" para cumplir con ambos PDF/A-4 (ISO 19005-4:2020)
# y los estándares PDF/UA-2 (ISO 14289-2:2024).
# Establezca la propiedad "Compliance" a "PdfCompliance.PdfUa2" para cumplir con el estándar PDF/UA-2 (ISO 14289-2:2024).
# Esto ayuda a que los documentos sean buscables, pero puede aumentar significativamente el tamaño de documentos ya grandes.
save_options.compliance = pdf_compliance
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.Compliance.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

