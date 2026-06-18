---
title: FontFallbackSettings.build_automatic method
linktitle: build_automatic method
articleTitle: build_automatic method
second_title: Aspose.Words for Python
description: "FontFallbackSettings.build_automatic method. Automatically builds the fallback settings by scanning available fonts."
type: docs
weight: 10
url: /python-net/aspose.words.fonts/fontfallbacksettings/build_automatic/
---

## build_automatic() {#default}

Automatically builds the fallback settings by scanning available fonts.


```python
def build_automatic(self):
    ...
```

### Remarks

This method may produce non-optimal fallback settings. Fonts are checked by [
            Unicode Character Range](https://docs.microsoft.com/en-us/typography/opentype/spec/os2#ur) fields and not by the actual glyphs presence. Also Unicode ranges are checked individually 
and several ranges related to single language/script may use different fallback fonts.



### See Also

* module [aspose.words.fonts](../../)
* class [FontFallbackSettings](../)

