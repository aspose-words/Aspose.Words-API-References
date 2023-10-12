---
title: StructuredDocumentTag.BuildingBlockCategory
second_title: Aspose.Words for .NET API Referansı
description: StructuredDocumentTag mülk. Bunun için yapı taşının kategorisini belirtir SDT node. Olamazhükümsüz .
type: docs
weight: 30
url: /tr/net/aspose.words.markup/structureddocumenttag/buildingblockcategory/
---
## StructuredDocumentTag.BuildingBlockCategory property

Bunun için yapı taşının kategorisini belirtir **SDT** node. Olamaz`hükümsüz` .

```csharp
public string BuildingBlockCategory { get; set; }
```

### Notlar

Bu özelliğe erişim yalnızca şunun için işe yarayacaktır:BuildingBlockGallery ve DocPartObj SDT türleri. Bunun için salt okunurdur **SDT** belge parçası türünün.

Diğer tüm SDT türleri için istisna meydana gelecektir.

### Örnekler

Yapılandırılmış belge etiketinin yapı taşı olarak nasıl ekleneceğini ve kategorisi ile galerisinin nasıl ayarlanacağını gösterir.

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


