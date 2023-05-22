---
title: BasicTextShaperCache class
linktitle: BasicTextShaperCache class
articleTitle: BasicTextShaperCache class
second_title: Aspose.Words for Python
description: "aspose.words.shaping.BasicTextShaperCache class. Implements basic cache for [ITextShaper](../itextshaper/) instances"
type: docs
weight: 10
url: /python-net/aspose.words.shaping/basictextshapercache/
---

## BasicTextShaperCache class

Implements basic cache for [ITextShaper](../itextshaper/) instances. This class is thread-safe.



**Interfaces:** [ITextShaperFactory](../itextshaperfactory/)

### Constructors
| Name | Description |
| --- | --- |
| [BasicTextShaperCache(factory)](./__init__/#itextshaperfactory) | Wraps  and caches[ITextShaperFactory.get_text_shaper()](../itextshaperfactory/get_text_shaper/#str_int) results. |

### Methods

| Name | Description |
| --- | --- |
|[ get_text_shaper(font_path, face_index)](../itextshaperfactory/get_text_shaper/#str_int) | Returns new instance of a text shaper for the font specified by  and.<br>(Inherited from [ITextShaperFactory](../itextshaperfactory/)) |
|[ get_text_shaper(font_id, font_blob, face_index)](../itextshaperfactory/get_text_shaper/#str_bytes_int) | Returns new instance of a text shaper for the font represented by  and.<br>(Inherited from [ITextShaperFactory](../itextshaperfactory/)) |

### See Also

* module [aspose.words.shaping](../)
* class [ITextShaperFactory](../itextshaperfactory/)

