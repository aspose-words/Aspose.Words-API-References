---
title: ParagraphFormat.space_before_auto property
linktitle: space_before_auto property
articleTitle: space_before_auto property
second_title: Aspose.Words for Python
description: "ParagraphFormat.space_before_auto property. True if the amount of spacing before the paragraph is set automatically."
type: docs
weight: 340
url: /ar/python-net/aspose.words/paragraphformat/space_before_auto/
---

## ParagraphFormat.space_before_auto property

True if the amount of spacing before the paragraph is set automatically.


```python
@property
def space_before_auto(self) -> bool:
    ...

@space_before_auto.setter
def space_before_auto(self, value: bool):
    ...

```

### Remarks

When set to ``True``, overrides the effect of [ParagraphFormat.space_before](../space_before/).




When you set paragraph Space Before and Space After to Auto,
Microsoft Word adds 14 points spacing between paragraphs automatically
according to the following rules:


* Normally, spacing is added after all paragraphs.
  
* In a bulleted or numbered list, spacing is added only after the last item in the list.
  Spacing is not added between the list items.
  
* In a nested bulleted or numbered list spacing is not added.
  
* Spacing is normally added after a table.
  
* Spacing is not added after a table if it is the last block in a table cell.
  
* Spacing is not added after the last paragraph in a table cell.
  



### Examples

Shows how to set automatic paragraph spacing.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# طبق مقدارًا كبيرًا من التباعد قبل وبعد الفقرات التي سيُنشئها هذا المُنشئ.
builder.paragraph_format.space_before = 24
builder.paragraph_format.space_after = 24
# اضبط هذه العلامات إلى "true" لتطبيق التباعد التلقائي،
# مما يتجاهل فعليًا التباعد في الخصائص التي ضبطناها أعلاه.
# تركها على "false" سيطبق تباعد الفقرة المخصص لدينا.
builder.paragraph_format.space_after_auto = auto_spacing
builder.paragraph_format.space_before_auto = auto_spacing
# أدرج فقرتين سيكون لهما تباعد فوق وتحتهما ثم احفظ المستند.
builder.writeln('Paragraph 1.')
builder.writeln('Paragraph 2.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.ParagraphSpacingAuto.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

