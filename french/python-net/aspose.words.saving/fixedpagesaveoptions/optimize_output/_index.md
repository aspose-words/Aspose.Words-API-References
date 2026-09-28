---
title: FixedPageSaveOptions.optimize_output property
linktitle: optimize_output property
articleTitle: optimize_output property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.optimize_output property. Flag indicates whether it is required to optimize output"
type: docs
weight: 50
url: /fr/python-net/aspose.words.saving/fixedpagesaveoptions/optimize_output/
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
# Créez un objet "XpsSaveOptions" à transmettre à la méthode "Save" du document
# pour modifier la façon dont cette méthode convertit le document en .XPS.
save_options = aw.saving.XpsSaveOptions()
# Définissez la propriété "OptimizeOutput" sur "true" pour prendre des mesures telles que la suppression de canevas imbriqués ou vides
# et la concaténation de segments adjacents avec un formatage identique afin d'optimiser le contenu du document de sortie.
# Cela peut affecter l'apparence du document.
# Définissez la propriété "OptimizeOutput" sur "false" pour enregistrer le document normalement.
save_options.optimize_output = optimize_output
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.OptimizeOutput.xps', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

