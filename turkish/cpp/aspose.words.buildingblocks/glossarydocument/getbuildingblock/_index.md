---
title: "Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock yöntemi"
linktitle: "GetBuildingBlock"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock yöntemi. C++'ta belirtilen galeri, kategori ve adı kullanarak bir yapı bloğu bulur."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument::GetBuildingBlock method


Belirtilen galeri, kategori ve adı kullanarak bir building block bulur.

```cpp
System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock(Aspose::Words::BuildingBlocks::BuildingBlockGallery gallery, const System::String &category, const System::String &name)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| galeri | Aspose::Words::BuildingBlocks::BuildingBlockGallery | Galeri ölçütü. |
| kategori | const System::String\& | Kategori ölçütü. **null** olabilir, bu durumda karşılaştırma için kullanılmaz. |
| name | const System::String\& | Yapı bloğu adı ölçütü. |

### ReturnValue

Eşleşen yapı bloğu veya eşleşme bulunamazsa **null**.
## Açıklamalar


Bu, bu koleksiyondaki tüm yapı blokları üzerinde yineleme yapan ve belirtilen galeri, kategori ve ada uyan ilk yapı bloğunu döndüren bir kolaylık yöntemidir.

Microsoft Word, yapı bloklarını galerilere düzenler. Galeriler, [BuildingBlockGallery](../../buildingblockgallery/) enumu kullanılarak önceden tanımlanır. Her galeri içinde, yapı blokları bir veya daha fazla kategoriye düzenlenebilir. Kategori adı bir dizedir. Her yapı bloğunun bir adı vardır. Bir yapı bloğu adının benzersiz olması garanti edilmez.

## Ayrıca Bakınız

* Class [BuildingBlock](../../buildingblock/)
* Enum [BuildingBlockGallery](../../buildingblockgallery/)
* Class [GlossaryDocument](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
