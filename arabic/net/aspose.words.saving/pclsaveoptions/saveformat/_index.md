---
title: PclSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية SaveFormat في PclSaveOptions لحفظ المستندات بسهولة بتنسيق PCL، مما يضمن التوافق والإخراج عالي الجودة لمشاريعك.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/pclsaveoptions/saveformat/
---
## PclSaveOptions.SaveFormat property

يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا. لا يمكن أن يكون إلاPcl .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## أمثلة

يوضح كيفية تحويل العناصر المعقدة إلى صور نقطية أثناء حفظ مستند في PCL.

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
