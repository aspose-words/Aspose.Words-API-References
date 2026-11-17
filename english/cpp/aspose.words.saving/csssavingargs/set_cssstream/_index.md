---
title: Aspose::Words::Saving::CssSavingArgs::set_CssStream method
linktitle: set_CssStream
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::CssSavingArgs::set_CssStream method. Allows to specify the stream where the CSS information will be saved to in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.saving/csssavingargs/set_cssstream/
---
## CssSavingArgs::set_CssStream(const System::SharedPtr\<System::IO::Stream\> \&) method


Allows to specify the stream where the CSS information will be saved to.

```cpp
void Aspose::Words::Saving::CssSavingArgs::set_CssStream(const System::SharedPtr<System::IO::Stream> & value)
```

## Remarks


This property allows you to save CSS information to a stream.

The default value is **null**. This property doesn't suppress saving CSS information to a file or embedding to HTML document. To suppress exporting CSS use the [IsExportNeeded](../get_isexportneeded/) property.

Using [ICssSavingCallback](../../icsssavingcallback/) you cannot substitute CSS with another. It is intended only for saving CSS to a stream.
## See Also

* Class [CssSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## CssSavingArgs::set_CssStream(std::basic_ostream\<CharType, Traits\> \&) method


Allows to specify the stream where the CSS information will be saved to.

```cpp
template<typename CharType,typename Traits> void Aspose::Words::Saving::CssSavingArgs::set_CssStream(std::basic_ostream<CharType, Traits> & value)
```

## Remarks


This property allows you to save CSS information to a stream.

The default value is **null**. This property doesn't suppress saving CSS information to a file or embedding to HTML document. To suppress exporting CSS use the [IsExportNeeded](../get_isexportneeded/) property.

Using [ICssSavingCallback](../../icsssavingcallback/) you cannot substitute CSS with another. It is intended only for saving CSS to a stream.
## See Also

* Class [CssSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
