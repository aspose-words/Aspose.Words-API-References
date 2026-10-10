---
title: ParagraphFormat.lines_to_drop property
linktitle: lines_to_drop property
articleTitle: lines_to_drop property
second_title: Aspose.Words for Python
description: "ParagraphFormat.lines_to_drop property. Gets or sets the number of lines of the paragraph text used to calculate the drop cap height."
type: docs
weight: 230
url: /sv/python-net/aspose.words/paragraphformat/lines_to_drop/
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
# Ändra egenskapen "LinesToDrop" för att ange ett stycke som en drop cap,
# vilket kommer att göra det till en stor versal som kommer att dekorera nästa stycke.
# Ge den här egenskapen värdet 4 för att ge inledningsbokstaven höjden av fyra textrader.
builder.paragraph_format.lines_to_drop = 4
builder.writeln('H')
# Återställ egenskapen "LinesToDrop" till 0 för att göra nästa stycke till ett vanligt stycke.
# Texten i detta stycke kommer att flöda runt inledningsbokstaven.
builder.paragraph_format.lines_to_drop = 0
builder.writeln('ello world!')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.LinesToDrop.odt')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

