---
title: "Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock méthode"
linktitle: "GetBuildingBlock"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock méthode. Trouve un bloc de construction en utilisant la galerie, la catégorie et le nom spécifiés en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument::GetBuildingBlock method


Trouve un bloc de construction en utilisant la galerie, la catégorie et le nom spécifiés.

```cpp
System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock(Aspose::Words::BuildingBlocks::BuildingBlockGallery gallery, const System::String &category, const System::String &name)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| galerie | Aspose::Words::BuildingBlocks::BuildingBlockGallery | Les critères de la galerie. |
| catégorie | const System::String\& | Les critères de la catégorie. Peut être **null**, auquel cas ils ne seront pas utilisés pour la comparaison. |
| name | const System::String\& | Les critères du nom du bloc de construction. |

### ReturnValue

Le bloc de construction correspondant ou **null** si aucune correspondance n'a été trouvée.
## Remarques


Il s'agit d'une méthode pratique qui parcourt tous les blocs de construction de cette collection et renvoie le premier bloc de construction correspondant à la galerie, à la catégorie et au nom spécifiés.

Microsoft Word organise les blocs de construction en galeries. Les galeries sont prédéfinies à l'aide de l'énumération [BuildingBlockGallery](../../buildingblockgallery/). Dans chaque galerie, les blocs de construction peuvent être organisés en une ou plusieurs catégories. Le nom de la catégorie est une chaîne de caractères. Chaque bloc de construction possède un nom. Le nom d'un bloc de construction n'est pas garanti d'être unique.

## Voir aussi

* Class [BuildingBlock](../../buildingblock/)
* Enum [BuildingBlockGallery](../../buildingblockgallery/)
* Class [GlossaryDocument](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
