---
title: WarningInfo.warning_type property
linktitle: warning_type property
articleTitle: warning_type property
second_title: Aspose.Words for Python
description: "WarningInfo.warning_type property. Returns the type of the warning."
type: docs
weight: 30
url: /sv/python-net/aspose.words/warninginfo/warning_type/
---

## WarningInfo.warning_type property

Returns the type of the warning.


```python
@property
def warning_type(self) -> aspose.words.WarningType:
    ...

```

### Examples

Shows how to set the property for finding the closest match for a missing font from the available font sources.

```python
# Öppna ett dokument som innehåller text formaterad med ett teckensnitt som inte finns i någon av våra teckensnittskällor.
doc = aw.Document(file_name=MY_DIR + 'Missing font.docx')
# Tilldela en återuppringning för att hantera varningar om teckensnittsersättning.
warning_collector = aw.WarningInfoCollection()
doc.warning_callback = warning_collector
# Ange ett standardteckensnittsnamn och aktivera teckensnittsersättning.
font_settings = aw.fonts.FontSettings()
font_settings.substitution_settings.default_font_substitution.default_font_name = 'Arial'
font_settings.substitution_settings.font_info_substitution.enabled = True
# Ursprungliga teckensnittsmått bör användas efter teckensnittsersättning.
doc.layout_options.keep_original_font_metrics = True
# Vi får en varning om teckensnittsersättning om vi sparar ett dokument med ett saknat teckensnitt.
doc.font_settings = font_settings
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.EnableFontSubstitution.pdf')
for info in warning_collector:
    if info.warning_type == aw.WarningType.FONT_SUBSTITUTION:
        print(info.description)
```

### See Also

* module [aspose.words](../../)
* class [WarningInfo](../)

