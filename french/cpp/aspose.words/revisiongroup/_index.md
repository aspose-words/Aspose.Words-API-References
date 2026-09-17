---
title: "Aspose::Words::RevisionGroup class"
linktitle: "RevisionGroup"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::RevisionGroup class. Représente un groupe d'objets Revision séquentiels. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 54000
url: /fr/cpp/aspose.words/revisiongroup/
---
## RevisionGroup class


Représente un groupe d'objets [Revision](../revision/) séquentiels. Pour en savoir plus, consultez l'article de documentation [Suivi des modifications dans un document](https://docs.aspose.com/words/cpp/track-changes-in-a-document/).

```cpp
class RevisionGroup : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Author](./get_author/)() | Obtient l’auteur de ce groupe de révisions. |
| [get_RevisionType](./get_revisiontype/)() | Obtient le type de révisions incluses dans ce groupe. |
| [get_Text](./get_text/)() | Renvoie le texte inséré/supprimé/déplacé ou la description d’un changement de format. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
