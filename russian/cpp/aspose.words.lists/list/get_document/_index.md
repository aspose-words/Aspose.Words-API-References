---
title: "Aspose::Words::Lists::List::get_Document метод"
linktitle: "get_Document"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Lists::List::get_Document метод. Получает документ‑владельца в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.lists/list/get_document/
---
## List::get_Document method


Получает документ‑владельца.

```cpp
System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::Lists::List::get_Document() const
```

## Примечания


Список всегда имеет родительский документ и действителен только в контексте этого документа.

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

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
