---
title: "Aspose::Words::Lists::ListCollection::GetListByListId method"
linktitle: "GetListByListId"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Lists::ListCollection::GetListByListId method. Gibt eine Liste anhand einer Listenkennung in C++ zurück."
type: docs
weight: 11000
url: /de/cpp/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection::GetListByListId method


Ermittelt eine Liste anhand einer Listenkennung.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::GetListByListId(int32_t listId)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| listId | int32_t | Die Listenkennung. |

### ReturnValue

Gibt das Listenobjekt zurück. Gibt **null** zurück, wenn keine Liste mit der angegebenen Kennung gefunden wurde.
## Hinweise


Sie müssen diese Methode normalerweise nicht verwenden. Meistens wenden Sie die Listformatierung auf Absätze an, indem Sie einfach die [List](../../listformat/get_list/) Eigenschaft des [ListFormat](../../listformat/) Objekts einstellen.

## Beispiele



Zeigt, wie man die Eigenschaften des Besitzerdokuments von Listen überprüft.
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

## Siehe auch

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
