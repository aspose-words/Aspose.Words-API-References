---
title: MarkdownSaveOptions.ExportImagesAsBase64
linktitle: ExportImagesAsBase64
articleTitle: ExportImagesAsBase64
second_title: Aspose.Words لـ .NET
description: MarkdownSaveOptions ExportImagesAsBase64 ملكية. يحدد ما إذا كان سيتم حفظ الصور بتنسيق Base64 في ملف الإخراج. القيمة الافتراضية هيخطأ شنيع  في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/markdownsaveoptions/exportimagesasbase64/
---
## MarkdownSaveOptions.ExportImagesAsBase64 property

يحدد ما إذا كان سيتم حفظ الصور بتنسيق Base64 في ملف الإخراج. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

## ملاحظات

عندما يتم تعيين هذه الخاصية إلى`حقيقي` يتم تصدير بيانات الصور مباشرة إلى ملف**img** لا يتم إنشاء العناصر والملفات المنفصلة.

## أمثلة

يوضح كيفية حفظ مستند .md مع الصور المضمنة بداخله.

```csharp
Document doc = new Document(MyDir + "Images.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions { ExportImagesAsBase64 = exportImagesAsBase64 };

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportImagesAsBase64.md", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "MarkdownSaveOptions.ExportImagesAsBase64.md");

Assert.True(exportImagesAsBase64
    ? outDocContents.Contains("data:image/jpeg;base64")
    : outDocContents.Contains("MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg"));
```

### أنظر أيضا

* class [MarkdownSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
