---
title: MemoryFontSource constructor
linktitle: MemoryFontSource constructor
articleTitle: MemoryFontSource constructor
second_title: Aspose.Words for Python
description: "aspose.words.fonts.MemoryFontSource constructor"
type: docs
weight: 10
url: /python-net/aspose.words.fonts/memoryfontsource/__init__/
---

## MemoryFontSource(font_data) {#bytes}

Ctor.


```python
def __init__(self, font_data: bytes):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| font_data | bytes |  |

## MemoryFontSource(font_data, priority) {#bytes_int}

Ctor.


```python
def __init__(self, font_data: bytes, priority: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| font_data | bytes |  |
| priority | int |  |

## MemoryFontSource(font_data, priority, cache_key) {#bytes_int_str}

Ctor.


```python
def __init__(self, font_data: bytes, priority: int, cache_key: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| font_data | bytes |  |
| priority | int |  |
| cache_key | str |  |

## Examples

Shows how to use a byte array with data from a font file as a font source.

```python
with open(MY_DIR + "Alte DIN 1451 Mittelschrift.ttf", "rb") as file:
    font_bytes = file.read()

memory_font_source = aw.fonts.MemoryFontSource(font_bytes, 0)

doc = aw.Document()
doc.font_settings = aw.fonts.FontSettings()
doc.font_settings.set_fonts_sources([memory_font_source])

self.assertEqual(aw.fonts.FontSourceType.MEMORY_FONT, memory_font_source.type)
self.assertEqual(0, memory_font_source.priority)
```

## See Also

* module [aspose.words.fonts](../../)
* class [MemoryFontSource](../)

