---
title: "Aspose::Words::RevisionGroupCollection classe"
linktitle: "RevisionGroupCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::RevisionGroupCollection classe. Une collection d'objets RevisionGroup qui représentent des groupes de révisions dans le document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 55000
url: /fr/cpp/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class


Une collection d'objets [RevisionGroup](../revisiongroup/) qui représentent des groupes de révisions dans le document. Pour en savoir plus, consultez l'article de documentation [Track Changes in a Document](https://docs.aspose.com/words/cpp/track-changes-in-a-document/).

```cpp
class RevisionGroupCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::RevisionGroup>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Renvoie le nombre de groupes de révisions dans la collection. |
| [GetEnumerator](./getenumerator/)() override | Renvoie un objet énumérateur. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Renvoie un groupe de révisions à l'index spécifié. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Description |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Remarques


Vous ne créez pas d'instances de cette classe directement. Utilisez la propriété [Groups](../revisioncollection/get_groups/) pour obtenir les groupes de révisions présents dans un document.

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


Montre comment obtenir un groupe de révisions dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

System::SharedPtr<Aspose::Words::RevisionGroup> revisionGroup = doc->get_Revisions()->get_Groups()->idx_get(0);
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
