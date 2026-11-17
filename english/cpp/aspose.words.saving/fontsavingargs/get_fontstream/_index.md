---
title: Aspose::Words::Saving::FontSavingArgs::get_FontStream method
linktitle: get_FontStream
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::FontSavingArgs::get_FontStream method. Allows to specify the stream where the font will be saved to in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.saving/fontsavingargs/get_fontstream/
---
## FontSavingArgs::get_FontStream method


Allows to specify the stream where the font will be saved to.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::FontSavingArgs::get_FontStream() const
```

## Remarks


This property allows you to save fonts to streams instead of files during HTML export.

The default value is **null**. When this property is **null**, the font will be saved to a file specified in the [FontFileName](../get_fontfilename/) property.

## See Also

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
