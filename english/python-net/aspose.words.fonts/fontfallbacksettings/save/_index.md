---
title: save method
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.fonts.FontFallbackSettings.save method"
type: docs
weight: 50
url: /python-net/aspose.words.fonts/fontfallbacksettings/save/
---

## save(output_stream) {#bytesio}

Saves the current fallback settings to stream.


```python
def save(self, output_stream: BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output_stream | BytesIO |  |

## save(file_name) {#str}

Saves the current fallback settings to file.


```python
def save(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |

## Examples

Shows how to load and save font fallback settings to/from a stream.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

# Load an XML document that defines a set of font fallback settings.
with open(MY_DIR + "Font fallback rules.xml", "rb") as font_fallback_stream:

    font_settings = aw.fonts.FontSettings()
    font_settings.fallback_settings.load(font_fallback_stream)

    doc.font_settings = font_settings

doc.save(ARTIFACTS_DIR + "FontSettings.load_font_fallback_settings_from_stream.pdf")

# Use a stream to save our document's current font fallback settings as an XML document.
with open(ARTIFACTS_DIR + "FallbackSettings.xml", "wb") as font_fallback_stream:

    doc.font_settings.fallback_settings.save(font_fallback_stream)
```

Shows how to load and save font fallback settings to/from an XML document in the local file system.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

# Load an XML document that defines a set of font fallback settings.
font_settings = aw.fonts.FontSettings()
font_settings.fallback_settings.load(MY_DIR + "Font fallback rules.xml")

doc.font_settings = font_settings
doc.save(ARTIFACTS_DIR + "FontSettings.load_font_fallback_settings_from_file.pdf")

# Save our document's current font fallback settings as an XML document.
doc.font_settings.fallback_settings.save(ARTIFACTS_DIR + "FallbackSettings.xml")
```

## See Also

* module [aspose.words.fonts](../../)
* class [FontFallbackSettings](../)

