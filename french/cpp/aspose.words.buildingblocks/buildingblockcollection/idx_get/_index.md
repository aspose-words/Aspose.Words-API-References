---
title: "Aspose::Words::BuildingBlocks::BuildingBlockCollection::idx_get méthode"
linktitle: "idx_get"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::BuildingBlocks::BuildingBlockCollection::idx_get méthode. Récupère un bloc de construction à l'index donné en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.buildingblocks/buildingblockcollection/idx_get/
---
## BuildingBlockCollection::idx_get method


Récupère un bloc de construction à l'index indiqué.

```cpp
System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> Aspose::Words::BuildingBlocks::BuildingBlockCollection::idx_get(int32_t index)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| index | int32_t | Un indice dans la liste des blocs de construction. |
## Remarques


L'index commence à zéro.

Les index négatifs sont autorisés et indiquent un accès depuis la fin de la collection. Par exemple, -1 signifie le dernier élément, -2 le deuxième avant le dernier, etc.

Si l'index est supérieur ou égal au nombre d'éléments dans la liste, cela renvoie une référence nulle.

Si l'index est négatif et que sa valeur absolue est supérieure au nombre d'éléments dans la liste, cela renvoie une référence nulle.

## Voir aussi

* Class [BuildingBlock](../../buildingblock/)
* Class [BuildingBlockCollection](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
