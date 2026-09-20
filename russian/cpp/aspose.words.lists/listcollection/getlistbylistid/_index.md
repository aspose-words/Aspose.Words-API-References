---
title: "Aspose::Words::Lists::ListCollection::GetListByListId method"
linktitle: "GetListByListId"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Lists::ListCollection::GetListByListId. Получает список по идентификатору списка в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection::GetListByListId method


Получает список по идентификатору списка.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::GetListByListId(int32_t listId)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| listId | int32_t | Идентификатор списка. |

### ReturnValue

Возвращает объект списка. Возвращает **null**, если список с указанным идентификатором не найден.
## Примечания


Обычно вам не нужно использовать этот метод. В большинстве случаев вы применяете форматирование списка к абзацам, просто задавая свойство [List](../../listformat/get_list/) объекта [ListFormat](../../listformat/).

## Примеры



Показывает, как проверить свойства документа‑владельца списков.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Lists::ListCollection> lists = doc->get_Lists();
ASPOSE_ASSERT_EQ(doc, lists->get_Document());

System::SharedPtr<Aspose::Words::Lists::List> list = lists->Add(Aspose::Words::Lists::ListTemplate::BulletDefault);
ASPOSE_ASSERT_EQ(doc, list->get_Document());

std::cout << (System::String(u"Current list count: ") + lists->get_Count()) << std::endl;
std::cout << (System::String(u"Is the first document list: ") + (System::ObjectExt::Equals(lists->idx_get(0), list))) << std::endl;
std::cout << (System::String(u"ListId: ") + list->get_ListId()) << std::endl;
std::cout << (System::String(u"List is the same by ListId: ") + (System::ObjectExt::Equals(lists->GetListByListId(1), list))) << std::endl;
```

## См. также

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
