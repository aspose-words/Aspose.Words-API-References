---
title: PclSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words لـ .NET
description: PclSaveOptions SaveFormat ملكية. يحدد التنسيق الذي سيتم حفظ المستند به في حالة استخدام كائن خيارات الحفظ هذا. يمكن أن يكون فقطPcl  في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/pclsaveoptions/saveformat/
---
## PclSaveOptions.SaveFormat property

يحدد التنسيق الذي سيتم حفظ المستند به في حالة استخدام كائن خيارات الحفظ هذا. يمكن أن يكون فقطPcl .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## أمثلة

يوضح كيفية تنقيط العناصر المعقدة أثناء حفظ مستند في PCL.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PclSaveOptions saveOptions = new PclSaveOptions
{
    SaveFormat = SaveFormat.Pcl,
    RasterizeTransformedElements = true
};

doc.Save(ArtifactsDir + "PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PclSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
