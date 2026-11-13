---
title: Style.paragraph_format property
linktitle: paragraph_format property
articleTitle: paragraph_format property
second_title: Aspose.Words for Python
description: "Style.paragraph_format property. Gets the paragraph formatting of the style."
type: docs
weight: 150
url: /es/python-net/aspose.words/style/paragraph_format/
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
# Crea un estilo de párrafo personalizado.
style = doc.styles.add(aw.StyleType.PARAGRAPH, 'MyStyle1')
style.font.size = 24
style.font.name = 'Verdana'
style.paragraph_format.space_after = 12
# Crea una lista y asegúrate de que los párrafos que usan este estilo la utilicen.
style.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
style.list_format.list_level_number = 0
# Aplica el estilo de párrafo al párrafo actual del constructor de documentos y luego agrega algo de texto.
builder.paragraph_format.style = style
builder.writeln('Hello World: MyStyle1, bulleted list.')
# Cambia el estilo del constructor de documentos a uno que no tenga formato de lista y escribe otro párrafo.
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
builder.writeln('Hello World: Normal.')
builder.document.save(file_name=ARTIFACTS_DIR + 'Styles.ParagraphStyleBulletedList.docx')
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

