---
title: LayoutOptions.keep_original_font_metrics property
linktitle: keep_original_font_metrics property
articleTitle: keep_original_font_metrics property
second_title: Aspose.Words for Python
description: "LayoutOptions.keep_original_font_metrics property. Gets or sets an indication of whether the original font metrics should be used after font substitution"
type: docs
weight: 70
url: /python-net/aspose.words.layout/layoutoptions/keep_original_font_metrics/
---

## LayoutOptions.keep_original_font_metrics property

Gets or sets an indication of whether the original font metrics should be used after font substitution.
Default is ``True``.



```python
@property
def keep_original_font_metrics(self) -> bool:
    ...

@keep_original_font_metrics.setter
def keep_original_font_metrics(self, value: bool):
    ...

```

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

* module [aspose.words.layout](../../)
* class [LayoutOptions](../)

