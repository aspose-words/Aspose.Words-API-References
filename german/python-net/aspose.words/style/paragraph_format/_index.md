---
title: Style.paragraph_format property
linktitle: paragraph_format property
articleTitle: paragraph_format property
second_title: Aspose.Words for Python
description: "Style.paragraph_format property. Gets the paragraph formatting of the style."
type: docs
weight: 150
url: /de/python-net/aspose.words/style/paragraph_format/
---

## Style.paragraph_format property

Gets the paragraph formatting of the style.


```python
@property
def paragraph_format(self) -> aspose.words.ParagraphFormat:
    ...

```

### Remarks

For character and list styles this property returns ``None``.




### Examples

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

