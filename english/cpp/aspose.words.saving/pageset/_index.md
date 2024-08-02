---
title: Aspose::Words::Saving::PageSet class
linktitle: PageSet
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PageSet class. Describes a random set of pages. To learn more, visit the  documentation article in C++.'
type: docs
weight: 20000
url: /cpp/aspose.words.saving/pageset/
---
## PageSet class


Describes a random set of pages. To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) documentation article.

```cpp
class PageSet : public System::Collections::Generic::IEnumerable<int32_t>
```

## Methods

| Method | Description |
| --- | --- |
| static [get_All](./get_all/)() | Gets a set with all the pages of the document in their original order. |
| static [get_Even](./get_even/)() | Gets a set with all the even pages of the document in their original order. |
| static [get_Odd](./get_odd/)() | Gets a set with all the odd pages of the document in their original order. |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageSet](./pageset/)(int32_t) | Creates an one-page set based on exact page index. |
| [PageSet](./pageset/)(const System::ArrayPtr\<int32_t\>\&) | Creates a page set based on exact page indices. |
| [PageSet](./pageset/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\&) | Creates a page set based on ranges. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
