---
title: Font.name_ascii property
linktitle: name_ascii property
articleTitle: name_ascii property
second_title: Aspose.Words for Python
description: "Font.name_ascii property. Returns or sets the font used for Latin text (characters with character codes from 0 (zero) through 127)."
type: docs
weight: 240
url: /ru/python-net/aspose.words/font/name_ascii/
---

## Font.name_ascii property

Returns or sets the font used for Latin text (characters with character codes from 0 (zero) through 127).


```python
@property
def name_ascii(self) -> str:
    ...

@name_ascii.setter
def name_ascii(self, value: str):
    ...

```

### Examples

Shows how Microsoft Word can combine two different fonts in one run.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Предположим пробег, который мы используем конструктор для вставки, используя эту конфигурацию шрифта
# содержит символы в диапазоне символов ASCII. В этом случае,
# он будет отображать эти символы, используя этот шрифт.
builder.font.name_ascii = 'Calibri'
# Если не указан другой шрифт, построитель также применит этот шрифт ко всем вставляемым им символам.
self.assertEqual('Calibri', builder.font.name)
# Укажите шрифт для всех символов за пределами диапазона ASCII.
# Идеально, если у этого шрифта будет глиф для каждого требуемого символа вне ASCII.
builder.font.name_other = 'Courier New'
# Вставьте фрагмент с одним словом, состоящим из символов ASCII, и одним словом со всеми символами за пределами этого диапазона.
# Каждый символ будет отображаться с использованием одного из шрифтов, в зависимости от.
builder.writeln('Hello, Привет')
doc.save(file_name=ARTIFACTS_DIR + 'Font.NameAscii.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)
* property [Font.name](../name/)

