---
title: "Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock метод"
linktitle: "GetBuildingBlock"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock метод. Находит строительный блок, используя указанные галерею, категорию и имя в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument::GetBuildingBlock method


Находит строительный блок, используя указанные галерею, категорию и имя.

```cpp
System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock(Aspose::Words::BuildingBlocks::BuildingBlockGallery gallery, const System::String &category, const System::String &name)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| галерея | Aspose::Words::BuildingBlocks::BuildingBlockGallery | Критерий галереи. |
| категория | const System::String\& | Критерий категории. Может быть **null**, в этом случае он не будет использоваться для сравнения. |
| name | const System::String\& | Критерий имени строительного блока. |

### ReturnValue

Соответствующий строительный блок или **null**, если совпадение не найдено.
## Примечания


Это удобный метод, который перебирает все строительные блоки в этой коллекции и возвращает первый блок, соответствующий указанным галерее, категории и имени.

Microsoft Word организует строительные блоки в галереи. Галереи предопределены с помощью перечисления [BuildingBlockGallery](../../buildingblockgallery/). В каждой галерее строительные блоки могут быть организованы в одну или несколько категорий. Имя категории представляет собой строку. Каждый строительный блок имеет имя. Имя строительного блока не гарантирует уникальность.

## См. также

* Class [BuildingBlock](../../buildingblock/)
* Enum [BuildingBlockGallery](../../buildingblockgallery/)
* Class [GlossaryDocument](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
