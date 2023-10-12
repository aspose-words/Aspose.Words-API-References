---
title: StructuredDocumentTag.BuildingBlockCategory
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTag ملكية. يحدد فئة الكتلة البرمجية الإنشائية لهذا الغرض المعاملة الخاصة والتفضيلية العقدة. لا يمكن أن يكونباطل .
type: docs
weight: 30
url: /ar/net/aspose.words.markup/structureddocumenttag/buildingblockcategory/
---
## StructuredDocumentTag.BuildingBlockCategory property

يحدد فئة الكتلة البرمجية الإنشائية لهذا الغرض **المعاملة الخاصة والتفضيلية** العقدة. لا يمكن أن يكون`باطل` .

```csharp
public string BuildingBlockCategory { get; set; }
```

### ملاحظات

الوصول إلى هذه الخاصية سوف يعمل فقط من أجلBuildingBlockGallery و DocPartObj أنواع المعاملة الخاصة والتفضيلية. وهي للقراءة فقط ل **المعاملة الخاصة والتفضيلية** من نوع جزء المستند.

بالنسبة لجميع أنواع SDT الأخرى، سيحدث استثناء.

### أمثلة

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
* مساحة الاسم [Aspose.Words.Markup](../../structureddocumenttag/)
* المجسم [Aspose.Words](../../../)


