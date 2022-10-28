---
title: auto_hyphenation property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets value determining whether automatic hyphenation is turned on for the document"
type: docs
weight: 20
url: /python-net/aspose.words.settings/hyphenationoptions/auto_hyphenation/
---

## HyphenationOptions.auto_hyphenation property

Gets or sets value determining whether automatic hyphenation is turned on for the document.
Default value for this property is ``False``.



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

