---
title: FontFallbackSettings.load method
linktitle: load method
articleTitle: load method
second_title: Aspose.Words for Python
description: "aspose.words.fonts.FontFallbackSettings.load method"
type: docs
weight: 20
url: /ar/python-net/aspose.words.fonts/fontfallbacksettings/load/
---

## load(file_name) {#str}

Loads font fallback settings from XML file.


```python
def load(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | Input file name. |

## load(stream) {#bytesio}

Loads fallback settings from XML stream.


```python
def load(self, stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO | Input stream. |

## Examples

Shows how to load and save font fallback settings to/from an XML document in the local file system.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# حمّل مستند XML يحدد مجموعة من إعدادات احتياطي الخط.
font_settings = aw.fonts.FontSettings()
font_settings.fallback_settings.load(file_name=MY_DIR + 'Font fallback rules.xml')
doc.font_settings = font_settings
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.LoadFontFallbackSettingsFromFile.pdf')
# احفظ إعدادات احتياطي الخط الحالية لمستندنا كملف XML.
doc.font_settings.fallback_settings.save(file_name=ARTIFACTS_DIR + 'FallbackSettings.xml')
```

Shows how to load and save font fallback settings to/from a stream.

```python
doc = aw.Document(MY_DIR + 'Rendering.docx')
# حمّل مستند XML يحدد مجموعة من إعدادات احتياطي الخط.
with open(MY_DIR + 'Font fallback rules.xml', 'rb') as font_fallback_stream:
    font_settings = aw.fonts.FontSettings()
    font_settings.fallback_settings.load(font_fallback_stream)
    doc.font_settings = font_settings
doc.save(ARTIFACTS_DIR + 'FontSettings.load_font_fallback_settings_from_stream.pdf')
# استخدم تدفقًا لحفظ إعدادات احتياطي الخط الحالية لمستندنا كملف XML.
with open(ARTIFACTS_DIR + 'FallbackSettings.xml', 'wb') as font_fallback_stream:
    doc.font_settings.fallback_settings.save(font_fallback_stream)
```

## See Also

* module [aspose.words.fonts](../../)
* class [FontFallbackSettings](../)

