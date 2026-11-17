---
title: Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded method
linktitle: get_IsSubsettingNeeded
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded method. Allows to specify whether the current font will be subsetted before exporting as a font resource in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.saving/fontsavingargs/get_issubsettingneeded/
---
## FontSavingArgs::get_IsSubsettingNeeded method


Allows to specify whether the current font will be subsetted before exporting as a font resource.

```cpp
bool Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded() const
```

## Remarks


[Fonts](../../../aspose.words.fonts/) can be exported as complete original font files or subsetted to include only the characters that are used in the document. Subsetting allows to reduce the resulting font resource size.

By default, Aspose.Words decides whether to perform subsetting or not by comparing the original font file size with the one specified in [FontResourcesSubsettingSizeThreshold](../../htmlsaveoptions/get_fontresourcessubsettingsizethreshold/). You can override this behavior for individual fonts by setting the [IsSubsettingNeeded](./) property. 
## See Also

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
