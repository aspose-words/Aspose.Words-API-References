---
title: "Aspose::Words::BuildingBlocks::BuildingBlockCollection classe"
linktitle: "BuildingBlockCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::BuildingBlocks::BuildingBlockCollection classe. Une collection d'objets BuildingBlock dans le document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.buildingblocks/buildingblockcollection/
---
## BuildingBlockCollection class


Une collection d'objets [BuildingBlock](../buildingblock/) dans le document. Pour en savoir plus, consultez l'article de documentation [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class BuildingBlockCollection : public Aspose::Words::NodeCollection
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ajoute un nœud à la fin de la collection. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Supprime tous les nœuds de cette collection et du document. |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Détermine si un nœud se trouve dans la collection. |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | Obtient le nombre de nœuds dans la collection. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | Fournit une itération simple de type "foreach" sur la collection de nœuds. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Récupère un bloc de construction à l'index indiqué. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Renvoie l'index basé sur zéro du nœud spécifié. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Insère un nœud dans la collection à l'index spécifié. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Supprime le nœud de la collection et du document. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | Supprime le nœud à l'index spécifié de la collection et du document. |
| [ToArray](./toarray/)() | Copie tous les blocs de construction de la collection dans un nouveau tableau de blocs de construction. |
| static [Type](./type/)() |  |
## Remarques


Vous ne créez pas d'instances de cette classe directement. Pour accéder à une collection de blocs de construction, utilisez la propriété [BuildingBlocks](../glossarydocument/get_buildingblocks/).

## Voir aussi

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
