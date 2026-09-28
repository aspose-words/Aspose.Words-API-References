---
title: Font.locale_id property
linktitle: locale_id property
articleTitle: locale_id property
second_title: Aspose.Words for Python
description: "Font.locale_id property. Gets or sets the locale identifier (language) of the formatted characters."
type: docs
weight: 200
url: /ar/python-net/aspose.words/font/locale_id/
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
# إذا قمنا بتعيين لغة الخط إلى الإنجليزية وأدخلنا بعض النص الروسي،
# فلن يتعرف مدقق الإملاء للغة الإنجليزية على النص وسيُصنّفه كخطأ إملائي.
builder.font.locale_id = 1033  # English (United States)
builder.writeln('Привет!')
# حدد لغة مطابقة للنص الذي سنضيفه لتطبيق مدقق الإملاء المناسب.
builder.font.locale_id = 1049  # Russian
builder.writeln('Привет!')
doc.save(file_name=ARTIFACTS_DIR + 'Font.LocaleId.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

