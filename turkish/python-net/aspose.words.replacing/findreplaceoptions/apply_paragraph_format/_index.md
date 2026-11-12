---
title: FindReplaceOptions.apply_paragraph_format property
linktitle: apply_paragraph_format property
articleTitle: apply_paragraph_format property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.apply_paragraph_format property. Paragraph formatting applied to new content."
type: docs
weight: 30
url: /tr/python-net/aspose.words.replacing/findreplaceoptions/apply_paragraph_format/
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
# Bul ve değiştir sürecini değiştirmek için bir "FindReplaceOptions" nesnesi kullanabiliriz.
options = aw.replacing.FindReplaceOptions()
# Her paragrafı sağa hizalamak için "Alignment" özelliğini "ParagraphAlignment.Right" olarak ayarlayın
# bul ve değiştirme işleminin bulduğu bir eşleşme içeren.
options.apply_paragraph_format.alignment = aw.ParagraphAlignment.RIGHT
# Paragraf sonundan hemen önceki her nokta işaretini ünlem işaretiyle değiştirin.
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

