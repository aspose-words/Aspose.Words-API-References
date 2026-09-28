---
title: Style.equals method
linktitle: equals method
articleTitle: equals method
second_title: Aspose.Words for Python
description: "Style.equals method. Compares with the specified style"
type: docs
weight: 230
url: /fr/python-net/aspose.words/style/equals/
---

## equals(style) {#style}

Compares with the specified style.
Styles Istds are compared for built-in styles only.
Styles defaults are not included in comparison.
Base style, linked style and next paragraph style are recursively compared.


```python
def equals(self, style: aspose.words.Style):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| style | [Style](../) |  |

### Examples

Shows how to use style aliases.

```python
doc = aw.Document(file_name=MY_DIR + 'Style with alias.docx')
# Ce document contient un style nommé "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
# Si le nom d'un style comporte plusieurs valeurs séparées par des virgules, chaque clause est un alias distinct.
style = doc.styles.get_by_name('MyStyle')
self.assertEqual(['MyStyle Alias 1', 'MyStyle Alias 2'], list(style.aliases))
self.assertEqual('Title', style.base_style_name)
self.assertEqual('MyStyle Char', style.linked_style_name)
# Nous pouvons référencer un style en utilisant son alias, ainsi que son nom.
self.assertEqual(doc.styles.get_by_name('MyStyle Alias 1'), doc.styles.get_by_name('MyStyle Alias 2'))
builder = aw.DocumentBuilder(doc=doc)
builder.move_to_document_end()
builder.paragraph_format.style = doc.styles.get_by_name('MyStyle Alias 1')
builder.writeln('Hello world!')
builder.paragraph_format.style = doc.styles.get_by_name('MyStyle Alias 2')
builder.write('Hello again!')
self.assertEqual(doc.first_section.body.paragraphs[0].paragraph_format.style, doc.first_section.body.paragraphs[1].paragraph_format.style)
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

