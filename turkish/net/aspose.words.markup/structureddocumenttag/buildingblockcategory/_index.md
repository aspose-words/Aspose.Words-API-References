---
title: StructuredDocumentTag.BuildingBlockCategory
linktitle: BuildingBlockCategory
articleTitle: BuildingBlockCategory
second_title: .NET için Aspose.Words
description: SDT düğümlerinde yapı taşı kategorilerini tanımlamak için gerekli olan StructuredDocumentTag BuildingBlockCategory özelliğini keşfedin. Belge yapınızı geliştirin!
type: docs
weight: 30
url: /tr/net/aspose.words.markup/structureddocumenttag/buildingblockcategory/
---
## StructuredDocumentTag.BuildingBlockCategory property

Bu yapı bloğunun kategorisini belirtir**SDT** node. olamaz`hükümsüz` .

```csharp
public string BuildingBlockCategory { get; set; }
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
