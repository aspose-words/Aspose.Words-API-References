---
title: Style.base_style_name property
linktitle: base_style_name property
articleTitle: base_style_name property
second_title: Aspose.Words for Python
description: "Style.base_style_name property. Gets/sets the name of the style this style is based on."
type: docs
weight: 30
url: /ru/python-net/aspose.words/style/base_style_name/
---

## Style.base_style_name property

Gets/sets the name of the style this style is based on.


```python
@property
def base_style_name(self) -> str:
    ...

@base_style_name.setter
def base_style_name(self, value: str):
    ...

```

### Remarks

This will be an empty string if the style is not based on any other style and it can be set
to an empty string.


### Examples

Shows how to use style aliases.

```python
doc = aw.Document(file_name=MY_DIR + 'Style with alias.docx')
# Этот документ содержит стиль с именем "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
# Если у имени стиля несколько значений, разделённых запятыми, каждый пункт является отдельным псевдонимом.
style = doc.styles.get_by_name('MyStyle')
self.assertEqual(['MyStyle Alias 1', 'MyStyle Alias 2'], list(style.aliases))
self.assertEqual('Title', style.base_style_name)
self.assertEqual('MyStyle Char', style.linked_style_name)
# Мы можем ссылаться на стиль, используя его псевдоним, а также его имя.
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

