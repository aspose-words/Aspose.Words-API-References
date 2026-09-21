---
title: "Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock-metod"
linktitle: "GetBuildingBlock"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock-metod. Hittar ett byggblock med hjälp av det angivna galleriet, kategorin och namnet i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument::GetBuildingBlock method


Hittar ett byggblock med hjälp av den angivna galleriet, kategorin och namnet.

```cpp
System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock(Aspose::Words::BuildingBlocks::BuildingBlockGallery gallery, const System::String &category, const System::String &name)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| galleri | Aspose::Words::BuildingBlocks::BuildingBlockGallery | Gallerikriterierna. |
| kategori | const System::String\& | Kriteriet för kategori. Kan vara **null**, i så fall kommer det inte att användas för jämförelse. |
| namn | const System::String\& | Kriteriet för byggblockets namn. |

### ReturnValue

Det matchande byggblocket eller **null** om ingen matchning hittades.
## Anmärkningar


Detta är en bekvämlighetsmetod som itererar över alla byggblock i denna samling och returnerar det första byggblocket som matchar den angivna galleriet, kategorin och namnet.

Microsoft Word organiserar byggblock i gallerier. Gallerierna är fördefinierade med hjälp av enumen [BuildingBlockGallery](../../buildingblockgallery/). Inom varje galleri kan byggblock organiseras i en eller flera kategorier. Kategorinamnet är en sträng. Varje byggblock har ett namn. Ett byggblocks namn är inte garanterat unikt.

## Se även

* Class [BuildingBlock](../../buildingblock/)
* Enum [BuildingBlockGallery](../../buildingblockgallery/)
* Class [GlossaryDocument](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
