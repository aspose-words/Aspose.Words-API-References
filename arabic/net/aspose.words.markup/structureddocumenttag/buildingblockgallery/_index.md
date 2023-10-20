---
title: StructuredDocumentTag.BuildingBlockGallery
linktitle: BuildingBlockGallery
articleTitle: BuildingBlockGallery
second_title: Aspose.Words لـ .NET
description: StructuredDocumentTag BuildingBlockGallery ملكية. يحدد نوع الكتلة البرمجية الإنشائية لهذا الغرضالمعاملة الخاصة والتفضيلية . لا يمكن أن يكونباطل  في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.markup/structureddocumenttag/buildingblockgallery/
---
## StructuredDocumentTag.BuildingBlockGallery property

يحدد نوع الكتلة البرمجية الإنشائية لهذا الغرض**المعاملة الخاصة والتفضيلية** . لا يمكن أن يكون`باطل` .

```csharp
public string BuildingBlockGallery { get; set; }
```

## ملاحظات

الوصول إلى هذه الخاصية سوف يعمل فقط من أجلBuildingBlockGallery و DocPartObj أنواع المعاملة الخاصة والتفضيلية. وهي للقراءة فقط ل**المعاملة الخاصة والتفضيلية** من نوع جزء المستند.

بالنسبة لجميع أنواع SDT الأخرى، سيحدث استثناء.

## أمثلة

يوضح كيفية إدراج علامة مستند منظمة ككتلة إنشاء وتعيين فئتها ومعرضها.

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
