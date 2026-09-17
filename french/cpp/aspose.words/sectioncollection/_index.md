---
title: "Aspose::Words::SectionCollection classe"
linktitle: "SectionCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::SectionCollection class. Une collection d'objets Section dans le document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 59000
url: /fr/cpp/aspose.words/sectioncollection/
---
## SectionCollection class


Une collection d'objets [Section](../section/) dans le document. Pour en savoir plus, consultez l'article de documentation [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class SectionCollection : public Aspose::Words::NodeCollection
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ajoute un nœud à la fin de la collection. |
| [Clear](../nodecollection/clear/)() | Supprime tous les nœuds de cette collection et du document. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Détermine si un nœud se trouve dans la collection. |
| [get_Count](../nodecollection/get_count/)() | Obtient le nombre de nœuds dans la collection. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Fournit une itération simple de type "foreach" sur la collection de nœuds. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Récupère une section à l'index donné. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Renvoie l'index basé sur zéro du nœud spécifié. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Insère un nœud dans la collection à l'index spécifié. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Supprime le nœud de la collection et du document. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Supprime le nœud à l'index spécifié de la collection et du document. |
| [ToArray](./toarray/)() | Copie toutes les sections de la collection dans un nouveau tableau de sections. |
| static [Type](./type/)() |  |
## Remarques


Un document Microsoft Word peut contenir plusieurs sections. Pour créer une section dans Microsoft Word, sélectionnez la commande Insert/Break et choisissez un type de saut. Le saut indique si la section commence sur une nouvelle page ou sur la même page.

L'insertion et la suppression de sections par programmation peuvent être utilisées pour personnaliser les documents générés lors d'une fusion de courrier. Si un document doit contenir un contenu différent ou des parties du contenu selon certains critères, vous pouvez créer un document « master » qui contient plusieurs sections et supprimer certaines sections avant ou après la fusion de courrier.

## Exemples



Montre comment ajouter et supprimer des sections dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// Supprimez la première section du document.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// Ajoutez une copie de ce qui est maintenant la première section à la fin du document.
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## Voir aussi

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
