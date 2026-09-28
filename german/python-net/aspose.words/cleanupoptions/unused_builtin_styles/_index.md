---
title: CleanupOptions.unused_builtin_styles property
linktitle: unused_builtin_styles property
articleTitle: unused_builtin_styles property
second_title: Aspose.Words for Python
description: "CleanupOptions.unused_builtin_styles property. Specifies that unused [Style.built_in](../../style/built_in/) styles should be removed from document."
type: docs
weight: 30
url: /de/python-net/aspose.words/cleanupoptions/unused_builtin_styles/
---

## CleanupOptions.unused_builtin_styles property

Specifies that unused [Style.built_in](../../style/built_in/) styles should be removed from document.



```python
@property
def unused_builtin_styles(self) -> bool:
    ...

@unused_builtin_styles.setter
def unused_builtin_styles(self, value: bool):
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
# Kombiniert mit den integrierten Stilen hat das Dokument jetzt acht Stile.
# Ein benutzerdefinierter Stil wird als "verwendet" markiert, solange im Dokument Text vorhanden ist
# im selben Stil formatiert. Das bedeutet, dass die 4 von uns hinzugefügten Stile derzeit ungenutzt sind.
self.assertEqual(8, doc.styles.count)
# Wende einen benutzerdefinierten Zeichenstil an und anschließend einen benutzerdefinierten Liststil. Dadurch werden sie als "verwendet" markiert.
builder = aw.DocumentBuilder(doc=doc)
builder.font.style = doc.styles.get_by_name('MyParagraphStyle1')
builder.writeln('Hello world!')
doc_list = doc.lists.add(list_style=doc.styles.get_by_name('MyListStyle1'))
builder.list_format.list = doc_list
builder.writeln('Item 1')
builder.writeln('Item 2')
# Jetzt gibt es einen ungenutzten Zeichenstil und einen ungenutzten Liststil.
# Die Cleanup()-Methode kann, wenn sie mit einem CleanupOptions-Objekt konfiguriert ist, ungenutzte Stile anvisieren und entfernen.
cleanup_options = aw.CleanupOptions()
cleanup_options.unused_lists = True
cleanup_options.unused_styles = True
cleanup_options.unused_builtin_styles = True
doc.cleanup(cleanup_options)
self.assertEqual(4, doc.styles.count)
# Das Entfernen jedes Knotens, auf den ein benutzerdefinierter Stil angewendet wurde, markiert ihn erneut als "ungenutzt".
# Führe die Cleanup-Methode erneut aus, um sie zu entfernen.
doc.first_section.body.remove_all_children()
doc.cleanup(cleanup_options)
self.assertEqual(2, doc.styles.count)
```

### See Also

* module [aspose.words](../../)
* class [CleanupOptions](../)

