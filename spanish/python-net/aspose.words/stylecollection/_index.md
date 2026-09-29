---
title: StyleCollection class
linktitle: StyleCollection class
articleTitle: StyleCollection class
second_title: Aspose.Words for Python
description: "aspose.words.StyleCollection class. A collection of [Style](../style/) objects that represent both the built-in and user-defined styles in a document"
type: docs
weight: 1240
url: /es/python-net/aspose.words/stylecollection/
---

## StyleCollection class

A collection of [Style](../style/) objects that represent both the built-in and user-defined styles in a document.
To learn more, visit the [Working with Styles and Themes](https://docs.aspose.com/words/python-net/working-with-styles-and-themes/) documentation article.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets a style by index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of styles in the collection. |
| [default_font](./default_font/) | Gets document default text formatting. |
| [default_paragraph_format](./default_paragraph_format/) | Gets document default paragraph formatting. |
| [document](./document/) | Gets the owner document. |

### Methods

| Name | Description |
| --- | --- |
|[ add(type, name)](./add/#styletype_str) | Creates a new user defined style and adds it the collection. |
|[ add_copy(style)](./add_copy/#style) | Copies a style into this collection. |
|[ clear_quick_style_gallery()](./clear_quick_style_gallery/#default) | Removes all styles from the Quick Style Gallery panel. |
|[ get_by_name(name)](./get_by_name/#str) | Gets a style by name or alias. |
|[ get_by_style_identifier(sti)](./get_by_style_identifier/#styleidentifier) | Gets a built-in style by its locale independent identifier. |

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

* module [aspose.words](../)

