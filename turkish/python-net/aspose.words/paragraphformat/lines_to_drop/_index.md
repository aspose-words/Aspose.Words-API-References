---
title: ParagraphFormat.lines_to_drop property
linktitle: lines_to_drop property
articleTitle: lines_to_drop property
second_title: Aspose.Words for Python
description: "ParagraphFormat.lines_to_drop property. Gets or sets the number of lines of the paragraph text used to calculate the drop cap height."
type: docs
weight: 230
url: /tr/python-net/aspose.words/paragraphformat/lines_to_drop/
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
# "LinesToDrop" özelliğini değiştirerek bir paragrafı drop cap (ilk harf büyük) olarak belirleyin,
# bu, onu bir sonraki paragrafı süsleyecek büyük bir büyük harfe dönüştürecektir.
# Bu özelliğe 4 değerini vererek drop cap'in yüksekliğini dört metin satırı yapın.
builder.paragraph_format.lines_to_drop = 4
builder.writeln('H')
# "LinesToDrop" özelliğini 0'a sıfırlayarak bir sonraki paragrafı sıradan bir paragraf haline getirin.
# Bu paragraftaki metin drop cap'in etrafında kayacaktır.
builder.paragraph_format.lines_to_drop = 0
builder.writeln('ello world!')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.LinesToDrop.odt')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

