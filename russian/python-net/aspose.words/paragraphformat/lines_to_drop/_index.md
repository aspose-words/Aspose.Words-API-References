---
title: ParagraphFormat.lines_to_drop property
linktitle: lines_to_drop property
articleTitle: lines_to_drop property
second_title: Aspose.Words for Python
description: "ParagraphFormat.lines_to_drop property. Gets or sets the number of lines of the paragraph text used to calculate the drop cap height."
type: docs
weight: 230
url: /ru/python-net/aspose.words/paragraphformat/lines_to_drop/
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
# Измените свойство "LinesToDrop", чтобы обозначить абзац как броскую букву,
# что превратит его в большую заглавную букву, которая будет украшать следующий абзац.
# Установите значение этого свойства равным 4, чтобы задать высоту буквицы в четыре строки текста.
builder.paragraph_format.lines_to_drop = 4
builder.writeln('H')
# Сбросьте свойство \"LinesToDrop\" до 0, чтобы превратить следующий абзац в обычный абзац.
# Текст в этом абзаце будет обтекать буквицу.
builder.paragraph_format.lines_to_drop = 0
builder.writeln('ello world!')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.LinesToDrop.odt')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

