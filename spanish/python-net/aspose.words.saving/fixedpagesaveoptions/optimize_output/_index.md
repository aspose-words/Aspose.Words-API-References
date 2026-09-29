---
title: FixedPageSaveOptions.optimize_output property
linktitle: optimize_output property
articleTitle: optimize_output property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.optimize_output property. Flag indicates whether it is required to optimize output"
type: docs
weight: 50
url: /es/python-net/aspose.words.saving/fixedpagesaveoptions/optimize_output/
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
# Cree un objeto "XpsSaveOptions" para pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .XPS.
save_options = aw.saving.XpsSaveOptions()
# Establezca la propiedad "OptimizeOutput" a "true" para tomar medidas como eliminar lienzos anidados o vacíos
# y concatenar ejecuciones adyacentes con formato idéntico para optimizar el contenido del documento de salida.
# Esto puede afectar la apariencia del documento.
# Establezca la propiedad "OptimizeOutput" a "false" para guardar el documento normalmente.
save_options.optimize_output = optimize_output
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.OptimizeOutput.xps', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

