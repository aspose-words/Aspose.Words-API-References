---
title: StructuredDocumentTag.BuildingBlockGallery
linktitle: BuildingBlockGallery
articleTitle: BuildingBlockGallery
second_title: Aspose.Words для .NET
description: Откройте для себя свойство StructuredDocumentTag BuildingBlockGallery, определяющее тип строительного блока вашего SDT. Обеспечьте бесшовную настройку документа!
type: docs
weight: 40
url: /ru/net/aspose.words.markup/structureddocumenttag/buildingblockgallery/
---
## StructuredDocumentTag.BuildingBlockGallery property

Указывает тип строительного блока для этого**СДТ** . Не может быть`нулевой` .

```csharp
public string BuildingBlockGallery { get; set; }
```

## Примечания

Доступ к этому свойству будет возможен только дляBuildingBlockGallery и DocPartObj Типы SDT. Только для чтения**СДТ** части документа type.

Для всех остальных типов SDT возникнет исключение.

## Примеры

Показывает, как вставить структурированный тег документа в качестве строительного блока, а также задать его категорию и галерею.

```csharp
Document doc = new Document();

StructuredDocumentTag buildingBlockSdt =
    new StructuredDocumentTag(doc, SdtType.BuildingBlockGallery, MarkupLevel.Block)
    {
        BuildingBlockCategory = "Built-in",
        BuildingBlockGallery = "Table of Contents"
    };

doc.FirstSection.Body.AppendChild(buildingBlockSdt);

doc.Save(ArtifactsDir + "StructuredDocumentTag.BuildingBlockCategories.docx");
```

### Смотрите также

* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
