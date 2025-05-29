---
title: StructuredDocumentTag.BuildingBlockCategory
linktitle: BuildingBlockCategory
articleTitle: BuildingBlockCategory
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية StructuredDocumentTag BuildingBlockCategory، وهي أساسية لتحديد فئات كتل البناء في عقد SDT. حسّن بنية مستندك!
type: docs
weight: 30
url: /ar/net/aspose.words.markup/structureddocumenttag/buildingblockcategory/
---
## StructuredDocumentTag.BuildingBlockCategory property

يحدد فئة كتلة البناء لهذا**SDT** node. لا يمكن`باطل` .

```csharp
public string BuildingBlockCategory { get; set; }
```

## ملاحظات

سيتم الوصول إلى هذه الخاصية فقط لـBuildingBlockGallery و DocPartObj أنواع SDT. للقراءة فقط**SDT** من نوع جزء المستند.

بالنسبة لجميع أنواع SDT الأخرى، سيحدث استثناء.

## أمثلة

يوضح كيفية إدراج علامة مستند منظمة ككتلة بناء، وتعيين فئتها ومعرضها.

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

### أنظر أيضا

* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
