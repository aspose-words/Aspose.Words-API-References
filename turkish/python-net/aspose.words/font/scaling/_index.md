---
title: Font.scaling property
linktitle: scaling property
articleTitle: scaling property
second_title: Aspose.Words for Python
description: "Font.scaling property. Gets or sets character width scaling in percent."
type: docs
weight: 320
url: /tr/python-net/aspose.words/font/scaling/
---

## Font.scaling property

Gets or sets character width scaling in percent.


```python
@property
def scaling(self) -> int:
    ...

@scaling.setter
def scaling(self, value: int):
    ...

```

### Examples

Shows how to set horizontal scaling and spacing for characters.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Metin koşusu ekleyin ve karakter genişliğini %150'ye artırın.
builder.font.scaling = 150
builder.writeln('Wide characters')
# Metin koşusu ekleyin ve her karakter arasında 1pt ekstra yatay boşluk ekleyin.
builder.font.spacing = 1
builder.writeln('Expanded by 1pt')
# Metin koşusu ekleyin ve karakterleri 1pt daha yakınlaştırın.
builder.font.spacing = -1
builder.writeln('Condensed by 1pt')
doc.save(file_name=ARTIFACTS_DIR + 'Font.ScalingSpacing.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

