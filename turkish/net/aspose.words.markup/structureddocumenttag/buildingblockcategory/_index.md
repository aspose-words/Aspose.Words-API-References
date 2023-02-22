---
title: StructuredDocumentTag.BuildingBlockCategory
second_title: Aspose.Words for .NET API Referansı
description: StructuredDocumentTag mülk. Bunun için yapı taşı kategorisini belirtir SDT node. null olamaz.
type: docs
weight: 30
url: /tr/net/aspose.words.markup/structureddocumenttag/buildingblockcategory/
---
## StructuredDocumentTag.BuildingBlockCategory property

Bunun için yapı taşı kategorisini belirtir **SDT** node. null olamaz.

```csharp
public string BuildingBlockCategory { get; set; }
```

### Notlar

Bu mülke erişmek yalnızcaBuildingBlockGallery and DocPartObj SDT türleri. için salt okunurdur **SDT**belge parçası türünün.

Diğer tüm SDT türleri için istisna oluşacaktır.

### Örnekler

Yapı taşı olarak yapılandırılmış bir belge etiketinin nasıl ekleneceğini ve kategorisini ve galerisini nasıl ayarlayacağını gösterir.

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

### Ayrıca bakınız

* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../structureddocumenttag/)
* toplantı [Aspose.Words](../../../)


