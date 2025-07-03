---
title: Aspose::Words::Saving::PageSavingArgs::get_PageStream method
linktitle: get_PageStream
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PageSavingArgs::get_PageStream method. Allows to specify the stream where the document page will be saved to in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.saving/pagesavingargs/get_pagestream/
---
## PageSavingArgs::get_PageStream method


Allows to specify the stream where the document page will be saved to.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::PageSavingArgs::get_PageStream() const
```

## Remarks


This property allows you to save document pages to streams instead of files.

The default value is **null**. When this property is **null**, the document page will be saved to a file specified in the [PageFileName](../get_pagefilename/) property.

If both [PageStream](./) and [PageFileName](../get_pagefilename/) are set, then PageStream will be used.

## See Also

* Class [PageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
