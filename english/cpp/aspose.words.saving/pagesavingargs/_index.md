---
title: Aspose::Words::Saving::PageSavingArgs class
linktitle: PageSavingArgs
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PageSavingArgs class. Provides data for the PageSaving() event. To learn more, visit the  documentation article in C++.'
type: docs
weight: 19000
url: /cpp/aspose.words.saving/pagesavingargs/
---
## PageSavingArgs class


Provides data for the [PageSaving()](../ipagesavingcallback/pagesaving/) event. To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) documentation article.

```cpp
class PageSavingArgs : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_KeepPageStreamOpen](./get_keeppagestreamopen/)() const | Specifies whether Aspose.Words should keep the stream open or close it after saving a document page. |
| [get_PageFileName](./get_pagefilename/)() const | Gets the file name where the document page will be saved to. |
| [get_PageIndex](./get_pageindex/)() const | Current page index. |
| [get_PageStream](./get_pagestream/)() const | Allows to specify the stream where the document page will be saved to. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageSavingArgs](./pagesavingargs/)() |  |
| [set_KeepPageStreamOpen](./set_keeppagestreamopen/)(bool) | Setter for [Aspose::Words::Saving::PageSavingArgs::get_KeepPageStreamOpen](./get_keeppagestreamopen/). |
| [set_PageFileName](./set_pagefilename/)(const System::String\&) | Sets the file name where the document page will be saved to. |
| [set_PageStream](./set_pagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Setter for [Aspose::Words::Saving::PageSavingArgs::get_PageStream](./get_pagestream/). |
| [set_PageStream](./set_pagestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
