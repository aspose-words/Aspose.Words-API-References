---
title: ParagraphFormat.style property
linktitle: style property
articleTitle: style property
second_title: Aspose.Words for Python
description: "ParagraphFormat.style property. Gets or sets the paragraph style applied to this formatting."
type: docs
weight: 350
url: /de/python-net/aspose.words/paragraphformat/style/
---

## ParagraphFormat.style property

Gets or sets the paragraph style applied to this formatting.


```python
@property
def style(self) -> aspose.words.Style:
    ...

@style.setter
def style(self, value: aspose.words.Style):
    ...

```

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
* class [ParagraphFormat](../)

