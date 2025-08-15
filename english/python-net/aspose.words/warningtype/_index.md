---
title: WarningType enumeration
linktitle: WarningType enumeration
articleTitle: WarningType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.WarningType enumeration. Specifies the type of a warning that is issued by Aspose.Words during document loading or saving."
type: docs
weight: 1420
url: /python-net/aspose.words/warningtype/
---

## WarningType enumeration

Specifies the type of a warning that is issued by Aspose.Words during document loading or saving.


### Members

| Name | Description |
| --- | --- |
| DATA_LOSS_CATEGORY | Some text/char/image or other data will be missing from either the document tree following load,  or from the created document following save. |
| DATA_LOSS | Generic data loss, no specific code. |
| MAJOR_FORMATTING_LOSS_CATEGORY | The resulting document or a particular location in it might look substantially different  compared to the original document. |
| MAJOR_FORMATTING_LOSS | Generic major formatting loss, no specific code. |
| MINOR_FORMATTING_LOSS_CATEGORY | The resulting document or a particular location in it might look somewhat different compared  to the original document. |
| MINOR_FORMATTING_LOSS | Generic minor formatting loss, no specific code. |
| FONT_SUBSTITUTION | Font has been substituted. |
| FONT_EMBEDDING | Loss of embedded font information during document saving. |
| UNEXPECTED_CONTENT_CATEGORY | Some content in the source document could not be recognized (i.e. is unsupported), this may or may not  cause issues or result in data/formatting loss. |
| UNEXPECTED_CONTENT | Generic unexpected content, no specific code. |
| HINT | Advises of a potential problem or suggests an improvement. |

### Examples

Shows how to set the property for finding the closest match for a missing font from the available font sources.

```python
# Open a document that contains text formatted with a font that does not exist in any of our font sources.
doc = aw.Document(file_name=MY_DIR + 'Missing font.docx')
# Assign a callback for handling font substitution warnings.
warning_collector = aw.WarningInfoCollection()
doc.warning_callback = warning_collector
# Set a default font name and enable font substitution.
font_settings = aw.fonts.FontSettings()
font_settings.substitution_settings.default_font_substitution.default_font_name = 'Arial'
font_settings.substitution_settings.font_info_substitution.enabled = True
# Original font metrics should be used after font substitution.
doc.layout_options.keep_original_font_metrics = True
# We will get a font substitution warning if we save a document with a missing font.
doc.font_settings = font_settings
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.EnableFontSubstitution.pdf')
for info in warning_collector:
    if info.warning_type == aw.WarningType.FONT_SUBSTITUTION:
        print(info.description)
```

### See Also

* module [aspose.words](../)

