---
title: ParagraphFormat.outline_level property
linktitle: outline_level property
articleTitle: outline_level property
second_title: Aspose.Words for Python
description: "ParagraphFormat.outline_level property. Specifies the outline level of the paragraph in the document."
type: docs
weight: 260
url: /tr/python-net/aspose.words/paragraphformat/outline_level/
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
# Her paragrafın bir OutlineLevel'ı vardır; bu, 1 ile 9 arasında herhangi bir sayı olabileceği gibi varsayılan "BodyText" değerinde de olabilir.
# Özelliği numaralı değerlerden birine ayarlamak, sol tarafta bir ok gösterecektir.
# paragrafın başlangıcının.
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL1
builder.writeln('Paragraph outline level 1.')
# Seviye 1 en üst seviyedir. Daha yüksek bir seviyenin altında daha düşük seviyeli bir paragraf varsa,
# yüksek seviyeli paragrafı daraltmak, düşük seviyeli paragrafı da daraltacaktır.
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL2
builder.writeln('Paragraph outline level 2.')
# Aynı seviyedeki iki paragraf birbirini daraltmayacaktır,
# ve oklar, işaret ettikleri paragrafları daraltmaz.
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL3
builder.writeln('Paragraph outline level 3.')
builder.writeln('Paragraph outline level 3.')
# Varsayılan "BodyText" değeri en düşük seviyedir; herhangi bir seviyedeki paragraf bunu daraltabilir.
builder.paragraph_format.outline_level = aw.OutlineLevel.BODY_TEXT
builder.writeln('Paragraph at main text level.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.ParagraphOutlineLevel.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

