---
title: TxtSaveOptionsBase.force_page_breaks property
linktitle: force_page_breaks property
articleTitle: force_page_breaks property
second_title: Aspose.Words for Python
description: "TxtSaveOptionsBase.force_page_breaks property. Allows to specify whether the page breaks should be preserved during export."
type: docs
weight: 30
url: /fr/python-net/aspose.words.saving/txtsaveoptionsbase/force_page_breaks/
---

## TxtSaveOptionsBase.force_page_breaks property

Allows to specify whether the page breaks should be preserved during export.

The default value is ``False``.




```python
@property
def force_page_breaks(self) -> bool:
    ...

@force_page_breaks.setter
def force_page_breaks(self, value: bool):
    ...

```

### Remarks

The property affects only page breaks that are inserted explicitly into a document. 
It is not related to page breaks that MS Word automatically inserts at the end of each page.


### Examples

Shows how to specify whether to preserve page breaks when exporting a document to plaintext.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Page 1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 3')
# Créez un objet "TxtSaveOptions", que nous pouvons transmettre à la méthode "Save" du document
# méthode pour modifier la façon dont nous enregistrons le document en texte brut.
save_options = aw.saving.TxtSaveOptions()
# Les objets "Document" d'Aspose.Words ont des sauts de page, tout comme les documents Microsoft Word.
# Les formats d'enregistrement tels que ".txt" constituent un corps de texte continu sans sauts de page.
# Définissez la propriété "ForcePageBreaks" sur "true" pour conserver tous les sauts de page sous forme de caractères '\\f'.
# Définissez la propriété "ForcePageBreaks" sur "false" pour supprimer tous les sauts de page.
save_options.force_page_breaks = force_page_breaks
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.PageBreaks.txt', save_options=save_options)
# Si nous chargeons un document texte brut avec des sauts de page,
# l'objet "Document" les utilisera pour diviser le corps en pages.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.PageBreaks.txt')
self.assertEqual(3 if force_page_breaks else 1, doc.page_count)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptionsBase](../)

