---
title: Bibliography.bibliography_style property
linktitle: bibliography_style property
articleTitle: bibliography_style property
second_title: Aspose.Words for Python
description: "Bibliography.bibliography_style property. Gets or sets a string that represents the name of the active style to use for a bibliography."
type: docs
weight: 10
url: /python-net/aspose.words.bibliography/bibliography/bibliography_style/
---

## Bibliography.bibliography_style property

Gets or sets a string that represents the name of the active style to use for a bibliography.


```python
@property
def bibliography_style(self) -> str:
    ...

@bibliography_style.setter
def bibliography_style(self, value: str):
    ...

```

### Examples

Shows how to override built-in styles or provide custom one (BibliographyStylesProvider).

```python
class BibliographyStylesProvider(aw.fields.IBibliographyStylesProvider):

    def get_style(self, style_file_name):
        return system_helper.io.File.open_read(MY_DIR + 'Bibliography custom style.xsl')
```

### See Also

* module [aspose.words.bibliography](../../)
* class [Bibliography](../)

