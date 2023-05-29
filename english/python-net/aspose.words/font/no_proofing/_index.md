---
title: Font.no_proofing property
linktitle: no_proofing property
articleTitle: no_proofing property
second_title: Aspose.Words for Python
description: "Font.no_proofing property. True when the formatted characters are not to be spell checked."
type: docs
weight: 280
url: /python-net/aspose.words/font/no_proofing/
---

## Font.no_proofing property

True when the formatted characters are not to be spell checked.


### Examples

Shows how to prevent text from being spell checked by Microsoft Word.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Normally, Microsoft Word emphasizes spelling errors with a jagged red underline.
# We can un-set the "no_proofing" flag to create a portion of text that
# bypasses the spell checker while completely disabling it.
builder.font.no_proofing = True

builder.writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.")

doc.save(ARTIFACTS_DIR + "Font.no_proofing.docx")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

