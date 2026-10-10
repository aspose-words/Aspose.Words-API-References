---
title: CleanupOptions.unused_lists property
linktitle: unused_lists property
articleTitle: unused_lists property
second_title: Aspose.Words for Python
description: "CleanupOptions.unused_lists property. Specifies whether unused list and list definitions should be removed from document"
type: docs
weight: 40
url: /it/python-net/aspose.words/cleanupoptions/unused_lists/
---

## CleanupOptions.unused_lists property

Specifies whether unused list and list definitions should be removed from document.
Default value is ``True``.



```python
@property
def unused_lists(self) -> bool:
    ...

@unused_lists.setter
def unused_lists(self, value: bool):
    ...

```

### Examples

Shows how to remove all unused custom styles from a document.

```python
doc = aw.Document()
doc.styles.add(aw.StyleType.LIST, 'MyListStyle1')
doc.styles.add(aw.StyleType.LIST, 'MyListStyle2')
doc.styles.add(aw.StyleType.CHARACTER, 'MyParagraphStyle1')
doc.styles.add(aw.StyleType.CHARACTER, 'MyParagraphStyle2')
# Combinato con gli stili predefiniti, il documento ora ha otto stili.
# Uno stile personalizzato è contrassegnato come "usato" finché c'è del testo nel documento
# formattato con quello stile. Questo significa che i 4 stili che abbiamo aggiunto sono attualmente inutilizzati.
self.assertEqual(8, doc.styles.count)
# Applica uno stile di carattere personalizzato, e poi uno stile di elenco personalizzato. Facendo così li contrassegnerà come "usati".
builder = aw.DocumentBuilder(doc=doc)
builder.font.style = doc.styles.get_by_name('MyParagraphStyle1')
builder.writeln('Hello world!')
doc_list = doc.lists.add(list_style=doc.styles.get_by_name('MyListStyle1'))
builder.list_format.list = doc_list
builder.writeln('Item 1')
builder.writeln('Item 2')
# Ora, c'è uno stile di carattere inutilizzato e uno stile di elenco inutilizzato.
# Il metodo Cleanup() , quando configurato con un oggetto CleanupOptions, può mirare agli stili inutilizzati e rimuoverli.
cleanup_options = aw.CleanupOptions()
cleanup_options.unused_lists = True
cleanup_options.unused_styles = True
cleanup_options.unused_builtin_styles = True
doc.cleanup(cleanup_options)
self.assertEqual(4, doc.styles.count)
# Rimuovere ogni nodo a cui è applicato uno stile personalizzato lo contrassegna nuovamente come "inutilizzato".
# Esegui nuovamente il metodo Cleanup per rimuoverli.
doc.first_section.body.remove_all_children()
doc.cleanup(cleanup_options)
self.assertEqual(2, doc.styles.count)
```

### See Also

* module [aspose.words](../../)
* class [CleanupOptions](../)

