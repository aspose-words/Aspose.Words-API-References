---
title: ParagraphFormat.outline_level property
linktitle: outline_level property
articleTitle: outline_level property
second_title: Aspose.Words for Python
description: "ParagraphFormat.outline_level property. Specifies the outline level of the paragraph in the document."
type: docs
weight: 260
url: /ar/python-net/aspose.words/paragraphformat/outline_level/
---

## ParagraphFormat.outline_level property

Specifies the outline level of the paragraph in the document.


```python
@property
def outline_level(self) -> aspose.words.OutlineLevel:
    ...

@outline_level.setter
def outline_level(self, value: aspose.words.OutlineLevel):
    ...

```

### Examples

Shows how to configure paragraph outline levels to create collapsible text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# كل فقرة لديها OutlineLevel، والذي يمكن أن يكون أي رقم من 1 إلى 9، أو القيمة الافتراضية "BodyText".
# ضبط الخاصية على أحد القيم الرقمية سيظهر سهمًا إلى اليسار
# من بداية الفقرة.
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL1
builder.writeln('Paragraph outline level 1.')
# المستوى 1 هو أعلى مستوى. إذا كانت هناك فقرة ذات مستوى أقل تحت فقرة ذات مستوى أعلى،
# سيؤدي طي الفقرة ذات المستوى الأعلى إلى طي الفقرة ذات المستوى الأدنى.
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL2
builder.writeln('Paragraph outline level 2.')
# فقرتان من نفس المستوى لن تقوما بطي بعضهما البعض،
# والأسهم لا تقوم بطي الفقرات التي تشير إليها.
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL3
builder.writeln('Paragraph outline level 3.')
builder.writeln('Paragraph outline level 3.')
# القيمة الافتراضية "BodyText" هي الأدنى، والتي يمكن لأي فقرة من أي مستوى طيها.
builder.paragraph_format.outline_level = aw.OutlineLevel.BODY_TEXT
builder.writeln('Paragraph at main text level.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.ParagraphOutlineLevel.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

