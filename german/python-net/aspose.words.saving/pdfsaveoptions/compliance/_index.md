---
title: PdfSaveOptions.compliance property
linktitle: compliance property
articleTitle: compliance property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.compliance property. Specifies the PDF standards compliance level for output documents."
type: docs
weight: 50
url: /de/python-net/aspose.words.saving/pdfsaveoptions/compliance/
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
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
# Beachten Sie, dass einige PdfSaveOptions beim Speichern nach einem der Standards verboten und automatisch korrigiert werden.
# Verwenden Sie IWarningCallback, um zu erfahren, welche Optionen automatisch korrigiert werden.
save_options = aw.saving.PdfSaveOptions()
# Setzen Sie die Eigenschaft "Compliance" auf "PdfCompliance.PdfA1b", um dem Standard "PDF/A-1b" zu entsprechen,
# der darauf abzielt, das visuelle Erscheinungsbild des Dokuments zu erhalten, wie Aspose.Words es in PDF konvertiert.
# Setzen Sie die Eigenschaft "Compliance" auf "PdfCompliance.Pdf17", um dem Standard "1.7" zu entsprechen.
# Setzen Sie die "Compliance"-Eigenschaft auf "PdfCompliance.PdfA1a", um dem "PDF/A-1a"-Standard zu entsprechen,
# die mit "PDF/A-1b" konform ist und zudem die Dokumentenstruktur des Originaldokuments bewahrt.
# Setzen Sie die "Compliance"-Eigenschaft auf "PdfCompliance.PdfUa1", um dem "PDF/UA-1" (ISO 14289-1)-Standard zu entsprechen,
# die darauf abzielt, elektronische Dokumente im PDF zu definieren, die die Zugänglichkeit der Datei ermöglichen.
# Setzen Sie die "Compliance"-Eigenschaft auf "PdfCompliance.Pdf20", um dem "PDF 2.0" (ISO 32000-2)-Standard zu entsprechen.
# Setzen Sie die "Compliance"-Eigenschaft auf "PdfCompliance.PdfA4", um dem "PDF/A-4" (ISO 19004:2020)-Standard zu entsprechen,
# die die statische visuelle Erscheinung des Dokuments über die Zeit bewahrt.
# Setzen Sie die "Compliance"-Eigenschaft auf "PdfCompliance.PdfA4Ua2", um sowohl PDF/A-4 (ISO 19005-4:2020) zu entsprechen
# und PDF/UA-2 (ISO 14289-2:2024)-Standards.
# Setzen Sie die "Compliance"-Eigenschaft auf "PdfCompliance.PdfUa2", um dem PDF/UA-2 (ISO 14289-2:2024)-Standard zu entsprechen.
# Dies hilft dabei, Dokumente durchsuchbar zu machen, kann jedoch die Größe bereits großer Dokumente erheblich erhöhen.
save_options.compliance = pdf_compliance
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.Compliance.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

