---
title: TxtSaveOptionsBase.force_page_breaks property
linktitle: force_page_breaks property
articleTitle: force_page_breaks property
second_title: Aspose.Words for Python
description: "TxtSaveOptionsBase.force_page_breaks property. Allows to specify whether the page breaks should be preserved during export."
type: docs
weight: 30
url: /it/python-net/aspose.words.saving/txtsaveoptionsbase/force_page_breaks/
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
# Crea un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
# metodo per modificare il modo in cui salviamo il documento in testo semplice.
save_options = aw.saving.TxtSaveOptions()
# Gli oggetti "Document" di Aspose.Words hanno interruzioni di pagina, proprio come i documenti Microsoft Word.
# I formati di salvataggio come ".txt" sono un unico corpo continuo di testo senza interruzioni di pagina.
# Imposta la proprietà "ForcePageBreaks" su "true" per preservare tutte le interruzioni di pagina nella forma dei caratteri '\\f'.
# Imposta la proprietà "ForcePageBreaks" su "false" per eliminare tutte le interruzioni di pagina.
save_options.force_page_breaks = force_page_breaks
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.PageBreaks.txt', save_options=save_options)
# Se carichiamo un documento di testo semplice con interruzioni di pagina,
# l'oggetto "Document" le utilizzerà per suddividere il corpo in pagine.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.PageBreaks.txt')
self.assertEqual(3 if force_page_breaks else 1, doc.page_count)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptionsBase](../)

