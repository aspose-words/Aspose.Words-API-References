---
title: "Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock metodo"
linktitle: "GetBuildingBlock"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock metodo. Trova un blocco di costruzione usando la galleria, la categoria e il nome specificati in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument::GetBuildingBlock method


Trova un building block utilizzando la galleria, la categoria e il nome specificati.

```cpp
System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock(Aspose::Words::BuildingBlocks::BuildingBlockGallery gallery, const System::String &category, const System::String &name)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| galleria | Aspose::Words::BuildingBlocks::BuildingBlockGallery | Il criterio della galleria. |
| categoria | const System::String\& | Il criterio della categoria. Può essere **null**, nel qual caso non verrà usato per il confronto. |
| name | const System::String\& | Il criterio del nome del blocco di costruzione. |

### ReturnValue

Il blocco di costruzione corrispondente o **null** se non è stato trovato alcun risultato.
## Note


Questo è un metodo di comodità che itera tutti i blocchi di costruzione in questa collezione e restituisce il primo blocco di costruzione che corrisponde alla galleria, alla categoria e al nome specificati.

Microsoft Word organizza i blocchi di costruzione in gallerie. Le gallerie sono predefinite usando l'enumerazione [BuildingBlockGallery](../../buildingblockgallery/). All'interno di ogni galleria, i blocchi di costruzione possono essere organizzati in una o più categorie. Il nome della categoria è una stringa. Ogni blocco di costruzione ha un nome. Un nome di blocco di costruzione non è garantito essere unico.

## Vedi anche

* Class [BuildingBlock](../../buildingblock/)
* Enum [BuildingBlockGallery](../../buildingblockgallery/)
* Class [GlossaryDocument](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
