---
title: "Метод Aspose::Words::Fonts::FontInfoCollection::Contains"
linktitle: "Contains"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fonts::FontInfoCollection::Contains. Определяет, содержит ли коллекция шрифт с заданным именем в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection::Contains method


Определяет, содержит ли коллекция шрифт с указанным именем.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::Contains(const System::String &name)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| name | const System::String\& | Регистронезависимое имя шрифта для поиска. |

### ReturnValue

**true** if the item is found in the collection; otherwise, **false**.

## Примеры



Показывает информацию о шрифтах, присутствующих в пустом документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Пустой документ содержит 3 шрифта по умолчанию. Каждый шрифт в документе
// будет иметь соответствующий объект FontInfo, который содержит детали об этом шрифте.
ASSERT_EQ(3, doc->get_FontInfos()->get_Count());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Times New Roman"));
ASSERT_EQ(204, doc->get_FontInfos()->idx_get(u"Times New Roman")->get_Charset());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Symbol"));
ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Arial"));
```

## См. также

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
