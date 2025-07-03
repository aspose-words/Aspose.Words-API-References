---
title: Aspose::Words::Saving::CssSavingArgs::get_CssStream method
linktitle: get_CssStream
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::CssSavingArgs::get_CssStream method. Allows to specify the stream where the CSS information will be saved to in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.saving/csssavingargs/get_cssstream/
---
## CssSavingArgs::get_CssStream method


Allows to specify the stream where the CSS information will be saved to.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::CssSavingArgs::get_CssStream() const
```

## Remarks


This property allows you to save CSS information to a stream.

The default value is **null**. This property doesn't suppress saving CSS information to a file or embedding to HTML document. To suppress exporting CSS use the [IsExportNeeded](../get_isexportneeded/) property.

Using [ICssSavingCallback](../../icsssavingcallback/) you cannot substitute CSS with another. It is intended only for saving CSS to a stream.

## See Also

* Class [CssSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
