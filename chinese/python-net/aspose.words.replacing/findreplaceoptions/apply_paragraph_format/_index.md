---
title: FindReplaceOptions.apply_paragraph_format property
linktitle: apply_paragraph_format property
articleTitle: apply_paragraph_format property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.apply_paragraph_format property. Paragraph formatting applied to new content."
type: docs
weight: 30
url: /zh/python-net/aspose.words.replacing/findreplaceoptions/apply_paragraph_format/
---

## FindReplaceOptions.apply_paragraph_format property

Paragraph formatting applied to new content.


```python
@property
def apply_paragraph_format(self) -> aspose.words.ParagraphFormat:
    ...

```

### Examples

Shows how to add formatting to paragraphs in which a find-and-replace operation has found matches.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Every paragraph that ends with a full stop like this one will be right aligned.')
builder.writeln('This one will not!')
builder.write('This one also will.')
paragraphs = doc.first_section.body.paragraphs
self.assertEqual(aw.ParagraphAlignment.LEFT, paragraphs[0].paragraph_format.alignment)
self.assertEqual(aw.ParagraphAlignment.LEFT, paragraphs[1].paragraph_format.alignment)
self.assertEqual(aw.ParagraphAlignment.LEFT, paragraphs[2].paragraph_format.alignment)
# 我们可以使用 "FindReplaceOptions" 对象来修改查找替换过程。
options = aw.replacing.FindReplaceOptions()
# 将 "Alignment" 属性设置为 "ParagraphAlignment.Right"，以右对齐每个段落
# 其中包含查找替换操作找到的匹配项的段落。
options.apply_paragraph_format.alignment = aw.ParagraphAlignment.RIGHT
# 将每个紧跟在段落换行前的句号替换为感叹号。
count = doc.range.replace(pattern='.&p', replacement='!&p', options=options)
self.assertEqual(2, count)
self.assertEqual(aw.ParagraphAlignment.RIGHT, paragraphs[0].paragraph_format.alignment)
self.assertEqual(aw.ParagraphAlignment.LEFT, paragraphs[1].paragraph_format.alignment)
self.assertEqual(aw.ParagraphAlignment.RIGHT, paragraphs[2].paragraph_format.alignment)
self.assertEqual('Every paragraph that ends with a full stop like this one will be right aligned!\r' + 'This one will not!\r' + 'This one also will!', doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

