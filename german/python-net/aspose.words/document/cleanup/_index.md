---
title: Document.cleanup method
linktitle: cleanup method
articleTitle: cleanup method
second_title: Aspose.Words for Python
description: "aspose.words.Document.cleanup method"
type: docs
weight: 590
url: /de/python-net/aspose.words/document/cleanup/
---

## cleanup() {#default}

Cleans unused styles and lists from the document.


```python
def cleanup(self):
    ...
```

## cleanup(options) {#cleanupoptions}

Cleans unused styles and lists from the document depending on given [CleanupOptions](../../cleanupoptions/).



```python
def cleanup(self, options: aspose.words.CleanupOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| options | [CleanupOptions](../../cleanupoptions/) |  |

## Examples

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

## See Also

* module [aspose.words](../../)
* class [Document](../)

