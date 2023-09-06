---
title: ParagraphFormat.suppress_auto_hyphens property
linktitle: suppress_auto_hyphens property
articleTitle: suppress_auto_hyphens property
second_title: Aspose.Words for Python
description: "ParagraphFormat.suppress_auto_hyphens property. Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings."
type: docs
weight: 370
url: /python-net/aspose.words/paragraphformat/suppress_auto_hyphens/
---

## ParagraphFormat.suppress_auto_hyphens property

Specifies whether the current paragraph should be exempted from any hyphenation which
is applied in the document settings.


### Examples

Shows how to suppress hyphenation for a paragraph.

```python
aw.Hyphenation.register_dictionary("de-CH", MY_DIR + "hyph_de_CH.dic")

self.assertTrue(aw.Hyphenation.is_dictionary_registered("de-CH"))

# Open a document containing text with a locale matching that of our dictionary.
# When we save this document to a fixed page save format, its text will have hyphenation.
doc = aw.Document(MY_DIR + "German text.docx")

# We can set the "suppress_auto_hyphens" property to "True" to disable hyphenation
# for a specific paragraph while keeping it enabled for the rest of the document.
# The default value for this property is "False",
# which means every paragraph by default uses hyphenation if any is available.
doc.first_section.body.first_paragraph.paragraph_format.suppress_auto_hyphens = suppress_auto_hyphens

doc.save(ARTIFACTS_DIR + "ParagraphFormat.suppress_hyphens.pdf")
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

