---
title: Font.locale_id property
linktitle: locale_id property
articleTitle: locale_id property
second_title: Aspose.Words for Python
description: "Font.locale_id property. Gets or sets the locale identifier (language) of the formatted characters."
type: docs
weight: 200
url: /zh/python-net/aspose.words/font/locale_id/
---

## Font.locale_id property

Gets or sets the locale identifier (language) of the formatted characters.


```python
@property
def locale_id(self) -> int:
    ...

@locale_id.setter
def locale_id(self, value: int):
    ...

```

### Remarks

For the list of locale identifiers see https://msdn.microsoft.com/en-us/library/cc233965.aspx


### Examples

Shows how to set the locale of the text that we are adding with a document builder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 如果我们将字体的语言环境设置为英语并插入一些俄语文本，
# 英语语言环境的拼写检查器将无法识别该文本，并将其标记为拼写错误。
builder.font.locale_id = 1033  # English (United States)
builder.writeln('Привет!')
# 为即将添加的文本设置匹配的语言环境，以使用相应的拼写检查器。
builder.font.locale_id = 1049  # Russian
builder.writeln('Привет!')
doc.save(file_name=ARTIFACTS_DIR + 'Font.LocaleId.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

