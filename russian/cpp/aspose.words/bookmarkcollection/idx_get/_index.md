---
title: "Метод Aspose::Words::BookmarkCollection::idx_get"
linktitle: "idx_get"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::BookmarkCollection::idx_get. Возвращает закладку по имени в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words/bookmarkcollection/idx_get/
---
## BookmarkCollection::idx_get(const System::String\&) method


Возвращает закладку по имени.

```cpp
System::SharedPtr<Aspose::Words::Bookmark> Aspose::Words::BookmarkCollection::idx_get(const System::String &bookmarkName)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | const System::String\& | Имя закладки без учёта регистра. |
## Примечания


Возвращает **null**, если закладка с указанным именем не найдена.

## См. также

* Class [Bookmark](../../bookmark/)
* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## BookmarkCollection::idx_get(int32_t) method


Возвращает закладку по указанному индексу.

```cpp
System::SharedPtr<Aspose::Words::Bookmark> Aspose::Words::BookmarkCollection::idx_get(int32_t index)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int32_t | Индекс в коллекции. |
## Примечания


Индекс начинается с нуля.

Отрицательные индексы допускаются и указывают доступ с конца коллекции. Например, -1 означает последний элемент, -2 — предпоследний и так далее.

Если индекс больше или равен количеству элементов в списке, возвращается нулевая ссылка.

Если индекс отрицательный и его абсолютное значение больше количества элементов в списке, возвращается нулевая ссылка.

## См. также

* Class [Bookmark](../../bookmark/)
* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
