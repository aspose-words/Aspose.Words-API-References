---
title: HtmlSaveOptions.ExportImagesAsBase64
linktitle: ExportImagesAsBase64
articleTitle: ExportImagesAsBase64
second_title: Aspose.Words لـ .NET
description: HtmlSaveOptions ExportImagesAsBase64 ملكية. يحدد ما إذا كان سيتم حفظ الصور بتنسيق Base64 إلى مخرجات HTML أو MHTML أو EPUB. الافتراضي هوخطأ شنيع  في C#.
type: docs
weight: 170
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportimagesasbase64/
---
## HtmlSaveOptions.ExportImagesAsBase64 property

يحدد ما إذا كان سيتم حفظ الصور بتنسيق Base64 إلى مخرجات HTML أو MHTML أو EPUB. الافتراضي هو`خطأ شنيع` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

## ملاحظات

عندما يتم تعيين هذه الخاصية إلى`حقيقي` يتم تصدير بيانات الصور مباشرة إلى ملف**img** لا يتم إنشاء العناصر والملفات المنفصلة.

## أمثلة

يوضح كيفية تضمين الخطوط داخل مستند HTML محفوظ.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportFontsAsBase64 = true,
    CssStyleSheetType = CssStyleSheetType.Embedded,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportFontsAsBase64.html", options);
```

يوضح كيفية حفظ مستند .html مع الصور المضمنة بداخله.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportImagesAsBase64 = exportImagesAsBase64,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportImagesAsBase64.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportImagesAsBase64.html");

Assert.True(exportImagesAsBase64
    ? outDocContents.Contains("<img src=\"data:image/png;base64")
    : outDocContents.Contains("<img src=\"HtmlSaveOptions.ExportImagesAsBase64.001.png\""));
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
