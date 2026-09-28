---
title: Style.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "Style.font property. Gets the character formatting of the style."
type: docs
weight: 60
url: /de/python-net/aspose.words/style/font/
---

## Style.font property

Gets the character formatting of the style.


```python
@property
def font(self) -> aspose.words.Font:
    ...

```

### Remarks

For list styles this property returns ``None``.




### Examples

Shows how to create and apply a custom style.

```python
doc = aw.Document()
style = doc.styles.add(aw.StyleType.PARAGRAPH, 'MyStyle')
style.font.name = 'Times New Roman'
style.font.size = 16
style.font.color = aspose.pydrawing.Color.navy
# Stil automatisch neu definieren.
style.automatically_update = True
builder = aw.DocumentBuilder(doc=doc)
# Wenden Sie einen der Stile aus dem Dokument auf den Absatz an, den der Dokumenten‑Builder erstellt.
builder.paragraph_format.style = doc.styles.get_by_name('MyStyle')
builder.writeln('Hello world!')
first_paragraph_style = doc.first_section.body.first_paragraph.paragraph_format.style
self.assertEqual(style, first_paragraph_style)
# Entfernen Sie unseren benutzerdefinierten Stil aus der Stilsammlung des Dokuments.
doc.styles.get_by_name('MyStyle').remove()
first_paragraph_style = doc.first_section.body.first_paragraph.paragraph_format.style
# Jeglicher Text, der einen entfernten Stil verwendet hat, wird zur Standardformatierung zurückkehren.
self.assertFalse(any([s.name == 'MyStyle' for s in doc.styles]))
self.assertEqual('Times New Roman', first_paragraph_style.font.name)
self.assertEqual(12, first_paragraph_style.font.size)
self.assertEqual(aspose.pydrawing.Color.empty().to_argb(), first_paragraph_style.font.color.to_argb())
```

Shows how to create and use a paragraph style with list formatting.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Erstellen Sie einen benutzerdefinierten Absatzstil.
style = doc.styles.add(aw.StyleType.PARAGRAPH, 'MyStyle1')
style.font.size = 24
style.font.name = 'Verdana'
style.paragraph_format.space_after = 12
# Erstellen Sie eine Liste und stellen Sie sicher, dass die Absätze, die diesen Stil verwenden, diese Liste benutzen.
style.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
style.list_format.list_level_number = 0
# Wenden Sie den Absatzstil auf den aktuellen Absatz des Dokumenten‑Builders an und fügen Sie anschließend etwas Text hinzu.
builder.paragraph_format.style = style
builder.writeln('Hello World: MyStyle1, bulleted list.')
# Ändern Sie den Stil des Dokumenten‑Builders zu einem, das keine Listformatierung enthält, und schreiben Sie einen weiteren Absatz.
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
builder.writeln('Hello World: Normal.')
builder.document.save(file_name=ARTIFACTS_DIR + 'Styles.ParagraphStyleBulletedList.docx')
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

