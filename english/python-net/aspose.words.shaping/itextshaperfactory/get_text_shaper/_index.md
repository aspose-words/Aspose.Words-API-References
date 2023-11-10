---
title: ITextShaperFactory.get_text_shaper method
linktitle: get_text_shaper method
articleTitle: get_text_shaper method
second_title: Aspose.Words for Python
description: "aspose.words.shaping.ITextShaperFactory.get_text_shaper method"
type: docs
weight: 10
url: /python-net/aspose.words.shaping/itextshaperfactory/get_text_shaper/
---

## get_text_shaper(font_path, face_index) {#str_int}

Returns new instance of a text shaper for the font specified by *fontPath* and*faceIndex*.


```python
def get_text_shaper(self, font_path: str, face_index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| font_path | str | An absolute path to the font file. |
| face_index | int | An index of the font face in the TrueType font collection, or 0 if specified font file is not TrueType font collection. |

## get_text_shaper(font_id, font_blob, face_index) {#str_bytes_int}

Returns new instance of a text shaper for the font represented by *fontBlob* and*faceIndex*.


```python
def get_text_shaper(self, font_id: str, font_blob: bytes, face_index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| font_id | str | A unique identifier that can be uniquely associated with the provided font *fontBlob*. |
| font_blob | bytes | Byte array with the font data. |
| face_index | int | An index of the font face in the TrueType font collection, or 0 if *fontBlob* is not TrueType font collection. |

## See Also

* module [aspose.words.shaping](../../)
* class [ITextShaperFactory](../)

