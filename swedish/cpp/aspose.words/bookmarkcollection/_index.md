---
title: "Aspose::Words::BookmarkCollection class"
linktitle: "BookmarkCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::BookmarkCollection-klass. En samling av Bookmark-objekt som representerar bokmärkena i det angivna intervallet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/bookmarkcollection/
---
## BookmarkCollection class


En samling av [Bookmark](../bookmark/) objekt som representerar bokmärkena i det angivna intervallet. För att lära dig mer, besök dokumentationsartikeln [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class BookmarkCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Bookmark>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Clear](./clear/)() | Tar bort alla bokmärken från denna samling och från dokumentet. |
| [get_Count](./get_count/)() | Returnerar antalet bokmärken i samlingen. |
| [GetEnumerator](./getenumerator/)() override | Returnerar ett enumerator-objekt. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Returnerar ett bokmärke på det angivna indexet. |
| [idx_get](./idx_get/)(const System::String\&) | Returnerar ett bokmärke efter namn. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Bookmark\>\&) | Tar bort det angivna bokmärket från dokumentet. |
| [Remove](./remove/)(const System::String\&) | Tar bort ett bokmärke med det angivna namnet. |
| [RemoveAt](./removeat/)(int32_t) | Tar bort ett bokmärke på det angivna indexet. |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
