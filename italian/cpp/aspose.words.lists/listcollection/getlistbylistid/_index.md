---
title: "Aspose::Words::Lists::ListCollection::GetListByListId metodo"
linktitle: "GetListByListId"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Lists::ListCollection::GetListByListId metodo. Ottiene una lista mediante un identificatore di lista in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection::GetListByListId method


Ottiene un elenco mediante un identificatore di elenco.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::GetListByListId(int32_t listId)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| listId | int32_t | L'identificatore della lista. |

### ReturnValue

Restituisce l'oggetto lista. Restituisce **null** se non è stata trovata una lista con l'identificatore specificato.
## Note


Normalmente non è necessario utilizzare questo metodo. La maggior parte delle volte si applica la formattazione delle liste ai paragrafi semplicemente impostando la proprietà [List](../../listformat/get_list/) dell'oggetto [ListFormat](../../listformat/).

## Esempi



Mostra come verificare le proprietà del documento proprietario delle liste.
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

## Vedi anche

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
