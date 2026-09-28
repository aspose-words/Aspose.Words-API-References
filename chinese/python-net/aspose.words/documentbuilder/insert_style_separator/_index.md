---
title: DocumentBuilder.insert_style_separator method
linktitle: insert_style_separator method
articleTitle: insert_style_separator method
second_title: Aspose.Words for Python
description: "DocumentBuilder.insert_style_separator method. Inserts style separator into the document."
type: docs
weight: 490
url: /zh/python-net/aspose.words/documentbuilder/insert_style_separator/
---

## insert_style_separator() {#default}

Inserts style separator into the document.


```python
def insert_style_separator(self):
    ...
```

### Remarks

This method allows to apply different paragraph styles to two different parts of a text line.


### Examples

Shows how to work with style separators.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 每个段落只能有一种样式。
# InsertStyleSeparator 方法允许我们绕过此限制。
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.write('This text is in a Heading style. ')
builder.insert_style_separator()
para_style = builder.document.styles.add(aw.StyleType.PARAGRAPH, 'MyParaStyle')
para_style.font.bold = False
para_style.font.size = 8
para_style.font.name = 'Arial'
builder.paragraph_format.style_name = para_style.name
builder.write('This text is in a custom style. ')
# 调用 InsertStyleSeparator 方法会创建另一个段落，
# 它可以拥有不同于前一个的样式。段落之间不会有换行。
# 输出文档中的文本将看起来像一个段落但包含两种样式。
self.assertEqual(2, doc.first_section.body.paragraphs.count)
self.assertEqual('Heading 1', doc.first_section.body.paragraphs[0].paragraph_format.style.name)
self.assertEqual('MyParaStyle', doc.first_section.body.paragraphs[1].paragraph_format.style.name)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertStyleSeparator.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

