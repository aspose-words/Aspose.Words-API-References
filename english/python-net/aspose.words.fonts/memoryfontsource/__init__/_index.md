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
| font_data | bytes | Binary font data. |

## MemoryFontSource(font_data, priority) {#bytes_int}

Ctor.


```python
def __init__(self, font_data: bytes, priority: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| font_data | bytes | Binary font data. |
| priority | int | Font source priority. See the [FontSourceBase.priority](../../fontsourcebase/priority/) property description for more information. |

## MemoryFontSource(font_data, priority, cache_key) {#bytes_int_str}

Ctor.


```python
def __init__(self, font_data: bytes, priority: int, cache_key: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| font_data | bytes | Binary font data. |
| priority | int | Font source priority. See the [FontSourceBase.priority](../../fontsourcebase/priority/) property description for more information. |
| cache_key | str | The key of this source in the cache. See [MemoryFontSource.cache_key](../cache_key/) property description for more information. |

## Examples

Shows how to use a byte array with data from a font file as a font source.

```python
font_bytes = system_helper.io.File.read_all_bytes(MY_DIR + 'Alte DIN 1451 Mittelschrift.ttf')
memory_font_source = aw.fonts.MemoryFontSource(font_data=font_bytes, priority=0)
doc = aw.Document()
doc.font_settings = aw.fonts.FontSettings()
doc.font_settings.set_fonts_sources(sources=[memory_font_source])
self.assertEqual(aw.fonts.FontSourceType.MEMORY_FONT, memory_font_source.type)
self.assertEqual(0, memory_font_source.priority)
```

## See Also

* module [aspose.words.fonts](../../)
* class [MemoryFontSource](../)

