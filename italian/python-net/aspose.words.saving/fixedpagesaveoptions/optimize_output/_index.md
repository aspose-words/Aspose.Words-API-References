---
title: FixedPageSaveOptions.optimize_output property
linktitle: optimize_output property
articleTitle: optimize_output property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.optimize_output property. Flag indicates whether it is required to optimize output"
type: docs
weight: 50
url: /it/python-net/aspose.words.saving/fixedpagesaveoptions/optimize_output/
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
# Crea un oggetto "XpsSaveOptions" da passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo converte il documento in .XPS.
save_options = aw.saving.XpsSaveOptions()
# Imposta la proprietà "OptimizeOutput" su "true" per adottare misure come la rimozione di canvas nidificati o vuoti
# e concatenare segmenti adiacenti con formattazione identica per ottimizzare il contenuto del documento di output.
# Ciò potrebbe influire sull'aspetto del documento.
# Imposta la proprietà "OptimizeOutput" su "false" per salvare il documento normalmente.
save_options.optimize_output = optimize_output
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.OptimizeOutput.xps', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

