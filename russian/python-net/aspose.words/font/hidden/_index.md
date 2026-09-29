---
title: Font.hidden property
linktitle: hidden property
articleTitle: hidden property
second_title: Aspose.Words for Python
description: "Font.hidden property. True if the font is formatted as hidden text."
type: docs
weight: 140
url: /ru/python-net/aspose.words/font/hidden/
---

## Font.hidden property

True if the font is formatted as hidden text.


```python
@property
def hidden(self) -> bool:
    ...

@hidden.setter
def hidden(self, value: bool):
    ...

```

### Examples

Shows how to create a run of hidden text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Если флаг Hidden установлен в true, любой текст, созданный с помощью этого объекта Font, будет невидим в документе.
# Мы не увидим и не выделим скрытый текст, пока не включим параметр "Hidden text".
# находится в Microsoft Word через "File" -> "Options" -> "Display". Текст всё равно будет присутствовать,
# и мы сможем получить доступ к этому тексту программно.
# Не рекомендуется использовать этот метод для скрытия конфиденциальной информации.
builder.font.hidden = True
builder.font.size = 36
builder.writeln('This text will not be visible in the document.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Hidden.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

