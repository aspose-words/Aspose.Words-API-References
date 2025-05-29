---
title: StructuredDocumentTag.BuildingBlockGallery
linktitle: BuildingBlockGallery
articleTitle: BuildingBlockGallery
second_title: .NET için Aspose.Words
description: SDT'nizin yapı taşı türünü tanımlayan StructuredDocumentTag BuildingBlockGallery özelliğini keşfedin. Sorunsuz belge özelleştirmesini sağlayın!
type: docs
weight: 40
url: /tr/net/aspose.words.markup/structureddocumenttag/buildingblockgallery/
---
## StructuredDocumentTag.BuildingBlockGallery property

Bu yapı bloğunun türünü belirtir**SDT** . olamaz`hükümsüz` .

```csharp
public string BuildingBlockGallery { get; set; }
```

## Notlar

Bu özelliğe erişim yalnızca şu amaçlar için çalışacaktır:BuildingBlockGallery ve DocPartObj SDT türleri. Salt okunurdur**SDT** belge parçası türünün.

Diğer tüm SDT tipleri için istisna oluşacaktır.

## Örnekler

Yapılandırılmış bir belge etiketinin yapı taşı olarak nasıl ekleneceğini ve kategorisinin ve galerisinin nasıl ayarlanacağını gösterir.

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
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
