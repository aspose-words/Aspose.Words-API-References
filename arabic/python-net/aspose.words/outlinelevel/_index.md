---
title: OutlineLevel enumeration
linktitle: OutlineLevel enumeration
articleTitle: OutlineLevel enumeration
second_title: Aspose.Words for Python
description: "aspose.words.OutlineLevel enumeration. Specifies the outline level of a paragraph in the document."
type: docs
weight: 890
url: /ar/python-net/aspose.words/outlinelevel/
---

## OutlineLevel enumeration

Specifies the outline level of a paragraph in the document.


### Members

| Name | Description |
| --- | --- |
| LEVEL1 | The paragraph is at the outline level 1 (topmost level). |
| LEVEL2 | The paragraph is at the outline level 2. |
| LEVEL3 | The paragraph is at the outline level 3. |
| LEVEL4 | The paragraph is at the outline level 4. |
| LEVEL5 | The paragraph is at the outline level 5. |
| LEVEL6 | The paragraph is at the outline level 6. |
| LEVEL7 | The paragraph is at the outline level 7. |
| LEVEL8 | The paragraph is at the outline level 8. |
| LEVEL9 | The paragraph is at the outline level 9. |
| BODY_TEXT | The paragraph is at the level of the main text. |

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

* module [aspose.words](../)

