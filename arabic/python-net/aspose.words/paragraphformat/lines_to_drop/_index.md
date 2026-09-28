---
title: ParagraphFormat.lines_to_drop property
linktitle: lines_to_drop property
articleTitle: lines_to_drop property
second_title: Aspose.Words for Python
description: "ParagraphFormat.lines_to_drop property. Gets or sets the number of lines of the paragraph text used to calculate the drop cap height."
type: docs
weight: 230
url: /ar/python-net/aspose.words/paragraphformat/lines_to_drop/
---

## ParagraphFormat.lines_to_drop property

Gets or sets the number of lines of the paragraph text used to calculate the drop cap height.


```python
@property
def lines_to_drop(self) -> int:
    ...

@lines_to_drop.setter
def lines_to_drop(self, value: int):
    ...

```

### Examples

Shows how to set the size of a drop cap.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# عدّل الخاصية "LinesToDrop" لتعيين فقرة كحرف أول كبير،
# التي ستحولها إلى حرف كبير سيزين الفقرة التالية.
# امنح هذه الخاصية القيمة 4 لتعيين ارتفاع الحرف الأول إلى أربعة أسطر نصية.
builder.paragraph_format.lines_to_drop = 4
builder.writeln('H')
# أعد ضبط الخاصية "LinesToDrop" إلى 0 لتحويل الفقرة التالية إلى فقرة عادية.
# النص في هذه الفقرة سيلف حول الحرف الأول.
builder.paragraph_format.lines_to_drop = 0
builder.writeln('ello world!')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.LinesToDrop.odt')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

