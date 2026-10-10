---
title: Style.list_format property
linktitle: list_format property
articleTitle: list_format property
second_title: Aspose.Words for Python
description: "Style.list_format property. Provides access to the list formatting properties of a paragraph style."
type: docs
weight: 110
url: /it/python-net/aspose.words/style/list_format/
---

## Style.list_format property

Provides access to the list formatting properties of a paragraph style.


```python
@property
def list_format(self) -> aspose.words.lists.ListFormat:
    ...

```

### Remarks

This property is only valid for paragraph styles.
For other style types this property returns ``None``.




### Examples

Shows how to create and use a paragraph style with list formatting.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Crea uno stile di paragrafo personalizzato.
style = doc.styles.add(aw.StyleType.PARAGRAPH, 'MyStyle1')
style.font.size = 24
style.font.name = 'Verdana'
style.paragraph_format.space_after = 12
# Crea un elenco e assicurati che i paragrafi che usano questo stile lo utilizzino.
style.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
style.list_format.list_level_number = 0
# Applica lo stile di paragrafo al paragrafo corrente del document builder, quindi aggiungi del testo.
builder.paragraph_format.style = style
builder.writeln('Hello World: MyStyle1, bulleted list.')
# Cambia lo stile del document builder con uno che non ha formattazione di elenco e scrivi un altro paragrafo.
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
builder.writeln('Hello World: Normal.')
builder.document.save(file_name=ARTIFACTS_DIR + 'Styles.ParagraphStyleBulletedList.docx')
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

