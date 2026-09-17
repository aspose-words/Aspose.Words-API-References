---
title: "Aspose::Words::RevisionGroupCollection::get_Count méthode"
linktitle: "get_Count"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::RevisionGroupCollection::get_Count méthode. Retourne le nombre de groupes de révision dans la collection en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words/revisiongroupcollection/get_count/
---
## RevisionGroupCollection::get_Count method


Renvoie le nombre de groupes de révisions dans la collection.

```cpp
int32_t Aspose::Words::RevisionGroupCollection::get_Count()
```


## Exemples



Montre comment imprimer les informations sur un groupe de révisions dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

ASSERT_EQ(7, doc->get_Revisions()->get_Groups()->get_Count());

for (auto&& group : doc->get_Revisions()->get_Groups())
{
    std::cout << System::String::Format(u"Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group->get_Author(), group->get_RevisionType(), group->get_Text()) << std::endl;
}
```

## Voir aussi

* Class [RevisionGroupCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
