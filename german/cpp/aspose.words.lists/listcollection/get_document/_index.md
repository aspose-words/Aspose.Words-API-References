---
title: "Aspose::Words::Lists::ListCollection::get_Document method"
linktitle: "get_Document"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Lists::ListCollection::get_Document method. Gibt das Besitzerdokument in C++ zurück."
type: docs
weight: 9000
url: /de/cpp/aspose.words.lists/listcollection/get_document/
---
## ListCollection::get_Document method


Ermittelt das übergeordnete Dokument.

```cpp
System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::Lists::ListCollection::get_Document() const
```


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

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
