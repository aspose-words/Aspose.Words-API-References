---
title: HyphenationOptions.consecutive_hyphen_limit property
linktitle: consecutive_hyphen_limit property
articleTitle: consecutive_hyphen_limit property
second_title: Aspose.Words for Python
description: "HyphenationOptions.consecutive_hyphen_limit property. Gets or sets the maximum number of consecutive lines that can end with hyphens"
type: docs
weight: 30
url: /python-net/aspose.words.settings/hyphenationoptions/consecutive_hyphen_limit/
---

## HyphenationOptions.consecutive_hyphen_limit property

Gets or sets the maximum number of consecutive lines that can end with hyphens.
Default value for this property is 0.


```python
@property
def consecutive_hyphen_limit(self) -> int:
    ...

@consecutive_hyphen_limit.setter
def consecutive_hyphen_limit(self, value: int):
    ...

```

### Remarks

If value of this property is set to 0, any number of consecutive lines can end with hyphens.

The property does not have effect when saving to fixed page formats e.g. PDF.




### Examples

Shows how to configure automatic hyphenation.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.size = 24
builder.writeln('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
doc.hyphenation_options.auto_hyphenation = True
doc.hyphenation_options.consecutive_hyphen_limit = 2
doc.hyphenation_options.hyphenation_zone = 720
doc.hyphenation_options.hyphenate_caps = True
doc.save(file_name=ARTIFACTS_DIR + 'Document.HyphenationOptions.docx')
```

### See Also

* module [aspose.words.settings](../../)
* class [HyphenationOptions](../)

