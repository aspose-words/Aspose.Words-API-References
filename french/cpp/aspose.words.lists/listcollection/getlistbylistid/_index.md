---
title: "Aspose::Words::Lists::ListCollection::GetListByListId method"
linktitle: "GetListByListId"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Lists::ListCollection::GetListByListId method. Obtient une liste par un identifiant de liste en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection::GetListByListId method


Obtient une liste par son identifiant de liste.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::GetListByListId(int32_t listId)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| listId | int32_t | L'identifiant de la liste. |

### ReturnValue

Renvoie l'objet liste. Renvoie **null** si aucune liste avec l'identifiant spécifié n'a été trouvée.
## Remarques


Vous n'avez généralement pas besoin d'utiliser cette méthode. La plupart du temps, vous appliquez le format de liste aux paragraphes simplement en définissant la propriété [List](../../listformat/get_list/) de l'objet [ListFormat](../../listformat/).

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

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
