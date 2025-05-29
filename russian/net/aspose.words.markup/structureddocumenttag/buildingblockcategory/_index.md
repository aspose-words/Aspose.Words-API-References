---
title: StructuredDocumentTag.BuildingBlockCategory
linktitle: BuildingBlockCategory
articleTitle: BuildingBlockCategory
second_title: Aspose.Words для .NET
description: Откройте для себя свойство StructuredDocumentTag BuildingBlockCategory, необходимое для определения категорий строительных блоков в узлах SDT. Улучшите структуру вашего документа!
type: docs
weight: 30
url: /ru/net/aspose.words.markup/structureddocumenttag/buildingblockcategory/
---
## StructuredDocumentTag.BuildingBlockCategory property

Указывает категорию строительного блока для этого**СДТ** node. Не может быть`нулевой` .

```csharp
public string BuildingBlockCategory { get; set; }
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
