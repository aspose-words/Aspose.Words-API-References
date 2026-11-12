---
title: Style.aliases property
linktitle: aliases property
articleTitle: aliases property
second_title: Aspose.Words for Python
description: "Style.aliases property. Gets all aliases of this style"
type: docs
weight: 10
url: /tr/python-net/aspose.words/style/aliases/
---

## Style.aliases property

Gets all aliases of this style. If style has no aliases then empty array of string is returned.


```python
@property
def aliases(self) -> List[str]:
    ...

```

### Examples

Shows how to use style aliases.

```python
doc = aw.Document(file_name=MY_DIR + 'Style with alias.docx')
# Bu belge, "MyStyle,MyStyle Alias 1,MyStyle Alias 2" adlı bir stil içerir.
# Bir stilin adı virgülle ayrılmış birden fazla değere sahipse, her bir bölüm ayrı bir takma ad olur.
style = doc.styles.get_by_name('MyStyle')
self.assertEqual(['MyStyle Alias 1', 'MyStyle Alias 2'], list(style.aliases))
self.assertEqual('Title', style.base_style_name)
self.assertEqual('MyStyle Char', style.linked_style_name)
# Bir stilin takma adını ve adını kullanarak ona başvurabiliriz.
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

