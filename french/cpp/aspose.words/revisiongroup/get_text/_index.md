---
title: "Aspose::Words::RevisionGroup::get_Text méthode"
linktitle: "get_Text"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::RevisionGroup::get_Text méthode. Retourne le texte inséré/supprimé/déplacé ou la description d'un changement de format en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/revisiongroup/get_text/
---
## RevisionGroup::get_Text method


Renvoie le texte inséré/supprimé/déplacé ou la description d’un changement de format.

```cpp
System::String Aspose::Words::RevisionGroup::get_Text()
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

* Class [RevisionGroup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
