---
title: "Aspose::Words::Lists::List::get_Document méthode"
linktitle: "get_Document"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Lists::List::get_Document méthode. Obtient le document propriétaire en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.lists/list/get_document/
---
## List::get_Document method


Obtient le document propriétaire.

```cpp
System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::Lists::List::get_Document() const
```

## Remarques


Une liste possède toujours un document parent et n’est valide que dans le contexte de ce document.

## Exemples



Montre comment vérifier les propriétés du document propriétaire des listes.
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

## Voir aussi

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
