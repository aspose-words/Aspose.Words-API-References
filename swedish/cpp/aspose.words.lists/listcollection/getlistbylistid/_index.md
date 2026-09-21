---
title: "Aspose::Words::Lists::ListCollection::GetListByListId metod"
linktitle: "GetListByListId"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Lists::ListCollection::GetListByListId metod. Hämtar en lista med ett listidentifierare i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection::GetListByListId method


Hämtar en lista med ett listidentifierare.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::GetListByListId(int32_t listId)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| listId | int32_t | Listidentifieraren. |

### ReturnValue

Returnerar listobjektet. Returnerar **null** om en lista med den angivna identifieraren inte hittades.
## Anmärkningar


Du behöver normalt inte använda den här metoden. Oftast applicerar du listformatering på stycken bara genom att ställa in [List](../../listformat/get_list/) egenskapen på [ListFormat](../../listformat/) objektet.

## Exempel



Visar hur man verifierar ägardokumentegenskaper för listor.
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

## Se även

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
