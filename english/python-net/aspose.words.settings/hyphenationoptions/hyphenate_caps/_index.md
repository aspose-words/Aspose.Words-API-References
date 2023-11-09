---
title: HyphenationOptions.hyphenate_caps property
linktitle: hyphenate_caps property
articleTitle: hyphenate_caps property
second_title: Aspose.Words for Python
description: "HyphenationOptions.hyphenate_caps property. Gets or sets value determining whether words written in all capital letters are hyphenated"
type: docs
weight: 40
url: /python-net/aspose.words.settings/hyphenationoptions/hyphenate_caps/
---

## HyphenationOptions.hyphenate_caps property

Gets or sets value determining whether words written in all capital letters are hyphenated.
Default value for this property is ``True``.



```python
@property
def hyphenate_caps(self) -> bool:
    ...

@hyphenate_caps.setter
def hyphenate_caps(self, value: bool):
    ...

```

### Examples

Shows how to configure automatic hyphenation.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.size = 24
builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.")

doc.hyphenation_options.auto_hyphenation = True
doc.hyphenation_options.consecutive_hyphen_limit = 2
doc.hyphenation_options.hyphenation_zone = 720
doc.hyphenation_options.hyphenate_caps = True

doc.save(ARTIFACTS_DIR + "Document.hyphenation_options.docx")
```

### See Also

* module [aspose.words.settings](../../)
* class [HyphenationOptions](../)

