---
title: PageSet
second_title: Aspose.Words for C++ API Reference
description: Describes a random set of pages.
type: docs
weight: 248
url: /cpp/aspose.words.saving/pageset/
---
## PageSet class


Describes a random set of pages.

```cpp
class PageSet : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| static [get_All](./get_all/)() | Gets a set with all the pages of the document in their original order. |
| static [get_Even](./get_even/)() | Gets a set with all the even pages of the document in their original order. |
| static [get_Odd](./get_odd/)() | Gets a set with all the odd pages of the document in their original order. |
| [PageSet](./pageset/)(int32_t) | Creates an one-page set based on exact page index. |
| [PageSet](./pageset/)(const System::ArrayPtr\<int32_t\>\&) | Creates a page set based on exact page indices. |
| [PageSet](./pageset/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\&) | Creates a page set based on ranges. |
