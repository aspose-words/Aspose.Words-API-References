---
title: PdfSaveOptions.compliance property
linktitle: compliance property
articleTitle: compliance property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.compliance property. Specifies the PDF standards compliance level for output documents."
type: docs
weight: 50
url: /fr/python-net/aspose.words.saving/pdfsaveoptions/compliance/
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
# Créez un objet "PdfSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont cette méthode convertit le document en .PDF.
# Notez que certaines PdfSaveOptions sont interdites lors de l'enregistrement selon l'une des normes et sont automatiquement corrigées.
# Utilisez IWarningCallback pour savoir quelles options sont automatiquement corrigées.
save_options = aw.saving.PdfSaveOptions()
# Définissez la propriété "Compliance" sur "PdfCompliance.PdfA1b" pour être conforme à la norme "PDF/A-1b",
# qui vise à préserver l'apparence visuelle du document tel que Aspose.Words le convertit en PDF.
# Définissez la propriété "Compliance" sur "PdfCompliance.Pdf17" pour être conforme à la norme "1.7".
# Définissez la propriété "Compliance" sur "PdfCompliance.PdfA1a" pour vous conformer à la norme "PDF/A-1a",
# qui se conforme à "PDF/A-1b" tout en préservant la structure du document original.
# Définissez la propriété "Compliance" sur "PdfCompliance.PdfUa1" pour vous conformer à la norme "PDF/UA-1" (ISO 14289-1),
# qui vise à définir la représentation des documents électroniques en PDF afin de rendre le fichier accessible.
# Définissez la propriété "Compliance" sur "PdfCompliance.Pdf20" pour vous conformer à la norme "PDF 2.0" (ISO 32000-2).
# Définissez la propriété "Compliance" sur "PdfCompliance.PdfA4" pour vous conformer à la norme "PDF/A-4" (ISO 19004:2020),
# qui préserve l'apparence visuelle statique du document au fil du temps.
# Définissez la propriété "Compliance" sur "PdfCompliance.PdfA4Ua2" pour vous conformer à la fois à PDF/A-4 (ISO 19005-4:2020)
# et aux normes PDF/UA-2 (ISO 14289-2:2024).
# Définissez la propriété "Compliance" sur "PdfCompliance.PdfUa2" pour vous conformer à la norme PDF/UA-2 (ISO 14289-2:2024).
# Cela aide à rendre les documents recherchables mais peut augmenter considérablement la taille de documents déjà volumineux.
save_options.compliance = pdf_compliance
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.Compliance.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

