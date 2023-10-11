---
title: StructuredDocumentTag.BuildingBlockCategory
second_title: Справочник по API Aspose.Words для .NET
description: StructuredDocumentTag свойство. Указывает категорию стандартного блока для этого СДТ node. Не может бытьнулевой .
type: docs
weight: 30
url: /ru/net/aspose.words.markup/structureddocumenttag/buildingblockcategory/
---
## StructuredDocumentTag.BuildingBlockCategory property

Указывает категорию стандартного блока для этого **СДТ** node. Не может быть`нулевой` .

```csharp
public string BuildingBlockCategory { get; set; }
```

### Примечания

Доступ к этому ресурсу будет работать только дляBuildingBlockGallery and DocPartObj Типы СДТ. Он доступен только для чтения для **СДТ** типа части документа.

Для всех остальных типов SDT возникнет исключение.

### Примеры

Показывает, как вставить тег структурированного документа в качестве стандартного блока и установить его категорию и галерею.

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
* пространство имен [Aspose.Words.Markup](../../structureddocumenttag/)
* сборка [Aspose.Words](../../../)


