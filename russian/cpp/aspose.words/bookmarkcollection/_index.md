---
title: "Класс Aspose::Words::BookmarkCollection"
linktitle: "BookmarkCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::BookmarkCollection. Коллекция объектов Bookmark, представляющих закладки в указанном диапазоне. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/bookmarkcollection/
---
## BookmarkCollection class


Коллекция объектов [Bookmark](../bookmark/), представляющих закладки в указанном диапазоне. Чтобы узнать больше, посетите статью документации [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class BookmarkCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Bookmark>>
```

## Методы

| Метод | Описание |
| --- | --- |
| [Clear](./clear/)() | Удаляет все закладки из этой коллекции и из документа. |
| [get_Count](./get_count/)() | Возвращает количество закладок в коллекции. |
| [GetEnumerator](./getenumerator/)() override | Возвращает объект перечислителя. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Возвращает закладку по указанному индексу. |
| [idx_get](./idx_get/)(const System::String\&) | Возвращает закладку по имени. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Bookmark\>\&) | Удаляет указанную закладку из документа. |
| [Remove](./remove/)(const System::String\&) | Удаляет закладку с указанным именем. |
| [RemoveAt](./removeat/)(int32_t) | Удаляет закладку по указанному индексу. |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
