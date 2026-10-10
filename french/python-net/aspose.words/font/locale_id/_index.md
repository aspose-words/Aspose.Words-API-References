---
title: Font.locale_id property
linktitle: locale_id property
articleTitle: locale_id property
second_title: Aspose.Words for Python
description: "Font.locale_id property. Gets or sets the locale identifier (language) of the formatted characters."
type: docs
weight: 200
url: /fr/python-net/aspose.words/font/locale_id/
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
# Si nous définissons la locale de la police sur anglais et insérons du texte russe,
# le correcteur orthographique de la locale anglaise ne reconnaîtra pas le texte et le signalera comme une faute d'orthographe.
builder.font.locale_id = 1033  # English (United States)
builder.writeln('Привет!')
# Définissez une locale correspondante pour le texte que nous allons ajouter afin d'appliquer le correcteur orthographique approprié.
builder.font.locale_id = 1049  # Russian
builder.writeln('Привет!')
doc.save(file_name=ARTIFACTS_DIR + 'Font.LocaleId.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

