---
title: FontSavingArgs.keep_font_stream_open property
linktitle: keep_font_stream_open property
articleTitle: keep_font_stream_open property
second_title: Aspose.Words for Python
description: "FontSavingArgs.keep_font_stream_open property. Specifies whether Aspose.Words should keep the stream open or close it after saving a font."
type: docs
weight: 90
url: /python-net/aspose.words.saving/fontsavingargs/keep_font_stream_open/
---

## FontSavingArgs.keep_font_stream_open property

Specifies whether Aspose.Words should keep the stream open or close it after saving a font.


```python
@property
def keep_font_stream_open(self) -> bool:
    ...

@keep_font_stream_open.setter
def keep_font_stream_open(self, value: bool):
    ...

```

### Remarks

Default is ``False`` and Aspose.Words will close the stream you provided
in the [FontSavingArgs.font_stream](../font_stream/) property after writing a font into it.
Specify ``True`` to keep the stream open.




### See Also

* module [aspose.words.saving](../../)
* class [FontSavingArgs](../)
* property [FontSavingArgs.font_stream](../font_stream/)

