﻿---
title: HyphenationOptions class
linktitle: HyphenationOptions class
articleTitle: HyphenationOptions class
second_title: Aspose.Words for Python
description: "aspose.words.settings.HyphenationOptions class. Allows to configure document hyphenation options"
type: docs
weight: 30
url: /python-net/aspose.words.settings/hyphenationoptions/
---

## HyphenationOptions class

Allows to configure document hyphenation options.
To learn more, visit the [Working with Hyphenation](https://docs.aspose.com/words/python-net/working-with-hyphenation/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [HyphenationOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [auto_hyphenation](./auto_hyphenation/) | Gets or sets value determining whether automatic hyphenation is turned on for the document. Default value for this property is ``False``. |
| [consecutive_hyphen_limit](./consecutive_hyphen_limit/) | Gets or sets the maximum number of consecutive lines that can end with hyphens. Default value for this property is 0. |
| [hyphenate_caps](./hyphenate_caps/) | Gets or sets value determining whether words written in all capital letters are hyphenated. Default value for this property is ``True``. |
| [hyphenation_zone](./hyphenation_zone/) | Gets or sets the distance in 1/20 of a point from the right margin within which you do not want to hyphenate words. Default value for this property is 360 (0.25 inch). |

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

* module [aspose.words.settings](../)

