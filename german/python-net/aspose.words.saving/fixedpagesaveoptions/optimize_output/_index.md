---
title: FixedPageSaveOptions.optimize_output property
linktitle: optimize_output property
articleTitle: optimize_output property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.optimize_output property. Flag indicates whether it is required to optimize output"
type: docs
weight: 50
url: /de/python-net/aspose.words.saving/fixedpagesaveoptions/optimize_output/
---

## FixedPageSaveOptions.optimize_output property

Flag indicates whether it is required to optimize output.
If this flag is set redundant nested canvases and empty canvases are removed,
also neighbor glyphs with the same formatting are concatenated.
Note: The accuracy of the content display may be affected if this property is set to ``True``.

Default is ``False``.



```python
@property
def optimize_output(self) -> bool:
    ...

@optimize_output.setter
def optimize_output(self, value: bool):
    ...

```

### Examples

Shows how to optimize document objects while saving to xps.

```python
doc = aw.Document(file_name=MY_DIR + 'Unoptimized document.docx')
# Erstellen Sie ein "XpsSaveOptions"-Objekt, um es an die "Save"-Methode des Dokuments zu übergeben
# um zu ändern, wie diese Methode das Dokument in .XPS konvertiert.
save_options = aw.saving.XpsSaveOptions()
# Setzen Sie die "OptimizeOutput"-Eigenschaft auf "true", um Maßnahmen wie das Entfernen verschachtelter oder leerer Leinwände zu ergreifen
# und das Zusammenführen benachbarter Abschnitte mit identischer Formatierung, um den Inhalt des Ausgabedokuments zu optimieren.
# Dies kann das Aussehen des Dokuments beeinflussen.
# Setzen Sie die "OptimizeOutput"-Eigenschaft auf "false", um das Dokument normal zu speichern.
save_options.optimize_output = optimize_output
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.OptimizeOutput.xps', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

