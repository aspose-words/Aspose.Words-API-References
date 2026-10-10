---
title: "Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock Methode"
linktitle: "GetBuildingBlock"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock Methode. Findet einen Baustein mithilfe der angegebenen Galerie, Kategorie und des Namens in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument::GetBuildingBlock method


Findet einen Baustein anhand der angegebenen Galerie, Kategorie und des Namens.

```cpp
System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock(Aspose::Words::BuildingBlocks::BuildingBlockGallery gallery, const System::String &category, const System::String &name)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Galerie | Aspose::Words::BuildingBlocks::BuildingBlockGallery | Die Galeriekriterien. |
| Kategorie | const System::String\& | Die Kriterien für die Kategorie. Kann **null** sein, in diesem Fall wird sie nicht zum Vergleich verwendet. |
| name | const System::String\& | Die Kriterien für den Namen des Bausteins. |

### ReturnValue

Der passende Baustein oder **null**, wenn kein Treffer gefunden wurde.
## Hinweise


Dies ist eine Hilfsmethode, die über alle Bausteine in dieser Sammlung iteriert und den ersten Baustein zurückgibt, der der angegebenen Galerie, Kategorie und dem Namen entspricht.

Microsoft Word organisiert Bausteine in Galerien. Die Galerien sind vordefiniert mittels des [BuildingBlockGallery](../../buildingblockgallery/) Enums. Innerhalb jeder Galerie können Bausteine in eine oder mehrere Kategorien organisiert werden. Der Kategoriename ist ein String. Jeder Baustein hat einen Namen. Ein Bausteinname ist nicht unbedingt eindeutig.

## Siehe auch

* Class [BuildingBlock](../../buildingblock/)
* Enum [BuildingBlockGallery](../../buildingblockgallery/)
* Class [GlossaryDocument](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
