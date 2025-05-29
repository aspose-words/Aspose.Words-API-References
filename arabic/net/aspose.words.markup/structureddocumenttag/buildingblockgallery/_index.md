---
title: StructuredDocumentTag.BuildingBlockGallery
linktitle: BuildingBlockGallery
articleTitle: BuildingBlockGallery
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية StructuredDocumentTag BuildingBlockGallery، التي تُحدد نوع كتلة البناء في SDT. خصص مستندك بسلاسة!
type: docs
weight: 40
url: /ar/net/aspose.words.markup/structureddocumenttag/buildingblockgallery/
---
## StructuredDocumentTag.BuildingBlockGallery property

يحدد نوع كتلة البناء لهذا**SDT** . لا يمكن`باطل` .

```csharp
public string BuildingBlockGallery { get; set; }
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
