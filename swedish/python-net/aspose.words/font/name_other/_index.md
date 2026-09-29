---
title: Font.name_other property
linktitle: name_other property
articleTitle: name_other property
second_title: Aspose.Words for Python
description: "Font.name_other property. Returns or sets the font used for characters with character codes from 128 through 255."
type: docs
weight: 270
url: /sv/python-net/aspose.words/font/name_other/
---

## Font.name_other property

Returns or sets the font used for characters with character codes from 128 through 255.


```python
@property
def name_other(self) -> str:
    ...

@name_other.setter
def name_other(self, value: str):
    ...

```

### Examples

Shows how Microsoft Word can combine two different fonts in one run.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Anta en körning som vi använder byggaren för att infoga medan vi använder denna teckensnittskonfiguration
# innehåller tecken inom ASCII-tecknens intervall. I så fall,
# den kommer att visa dessa tecken med detta teckensnitt.
builder.font.name_ascii = 'Calibri'
# Om inget annat teckensnitt anges kommer byggaren också att använda detta teckensnitt för alla tecken som den infogar.
self.assertEqual('Calibri', builder.font.name)
# Ange ett teckensnitt att använda för alla tecken utanför ASCII-intervallet.
# Idealiskt bör detta teckensnitt ha en glyf för varje nödvändig icke-ASCII-teckenkod.
builder.font.name_other = 'Courier New'
# Infoga ett körsegment med ett ord bestående av ASCII-tecken, och ett ord med alla tecken utanför det intervallet.
# Varje tecken kommer att visas med antingen det ena eller det andra teckensnittet, beroende på.
builder.writeln('Hello, Привет')
doc.save(file_name=ARTIFACTS_DIR + 'Font.NameAscii.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)
* property [Font.name](../name/)

