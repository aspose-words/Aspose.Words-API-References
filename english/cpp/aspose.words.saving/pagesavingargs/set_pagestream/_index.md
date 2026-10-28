---
title: Aspose::Words::Saving::PageSavingArgs::set_PageStream method
linktitle: set_PageStream
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PageSavingArgs::set_PageStream method. Allows to specify the stream where the document page will be saved to in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.saving/pagesavingargs/set_pagestream/
---
## PageSavingArgs::set_PageStream(const System::SharedPtr\<System::IO::Stream\> \&) method


Allows to specify the stream where the document page will be saved to.

```cpp
void Aspose::Words::Saving::PageSavingArgs::set_PageStream(const System::SharedPtr<System::IO::Stream> & value)
```

## Remarks


This property allows you to save document pages to streams instead of files.

The default value is **null**. When this property is **null**, the document page will be saved to a file specified in the [PageFileName](../get_pagefilename/) property.

If both [PageStream](../get_pagestream/) and [PageFileName](../get_pagefilename/) are set, then PageStream will be used.
## See Also

* Class [PageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## PageSavingArgs::set_PageStream(std::basic_ostream\<CharType, Traits\> \&) method


Allows to specify the stream where the document page will be saved to.

```cpp
template<typename CharType,typename Traits> void Aspose::Words::Saving::PageSavingArgs::set_PageStream(std::basic_ostream<CharType, Traits> & value)
```

## Remarks


This property allows you to save document pages to streams instead of files.

The default value is **null**. When this property is **null**, the document page will be saved to a file specified in the [PageFileName](../get_pagefilename/) property.

If both [PageStream](../get_pagestream/) and [PageFileName](../get_pagefilename/) are set, then PageStream will be used.
## See Also

* Class [PageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
