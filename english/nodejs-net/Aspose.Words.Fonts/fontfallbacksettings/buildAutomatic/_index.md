---
title: FontFallbackSettings.buildAutomatic method
linktitle: buildAutomatic method
articleTitle: buildAutomatic method
second_title: Aspose.Words for NodeJs
description: "FontFallbackSettings.buildAutomatic method. Automatically builds the fallback settings by scanning available fonts."
type: docs
weight: 10
url: /nodejs-net/aspose.words.fonts/fontfallbacksettings/buildAutomatic/
---

## buildAutomatic() {#default}

Automatically builds the fallback settings by scanning available fonts.


```js
buildAutomatic()
```

### Remarks

This method may produce non-optimal fallback settings. Fonts are checked by [
            Unicode Character Range](https://docs.microsoft.com/en-us/typography/opentype/spec/os2#ur) fields and not by the actual glyphs presence. Also Unicode ranges are checked individually 
and several ranges related to single language/script may use different fallback fonts.



### See Also

* module [Aspose.Words.Fonts](../../)
* class [FontFallbackSettings](../)

