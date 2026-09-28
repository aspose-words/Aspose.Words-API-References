---
title: FontFallbackSettings.save method
linktitle: save method
articleTitle: save method
second_title: Aspose.Words for Python
description: "aspose.words.fonts.FontFallbackSettings.save method"
type: docs
weight: 50
url: /ar/python-net/aspose.words.fonts/fontfallbacksettings/save/
---

## save(output_stream) {#bytesio}

Saves the current fallback settings to stream.


```python
def save(self, output_stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output_stream | io.BytesIO | Output stream. |

## save(file_name) {#str}

Saves the current fallback settings to file.


```python
def save(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | Output file name. |

## Examples

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

## See Also

* module [aspose.words.fonts](../../)
* class [FontFallbackSettings](../)

