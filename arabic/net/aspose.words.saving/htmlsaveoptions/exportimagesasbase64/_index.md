---
title: HtmlSaveOptions.ExportImagesAsBase64
linktitle: ExportImagesAsBase64
articleTitle: ExportImagesAsBase64
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية HtmlSaveOptions ExportImagesAsBase64 لحفظ الصور بتنسيق Base64 لتحسين جودة إخراجها بصيغ HTML أو MHTML أو EPUB. حسّن جودة مستندك!
type: docs
weight: 170
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportimagesasbase64/
---
## HtmlSaveOptions.ExportImagesAsBase64 property

يحدد ما إذا كان سيتم حفظ الصور بتنسيق Base64 في الإخراج HTML أو MHTML أو EPUB. الافتراضي هو`خطأ شنيع` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

## ملاحظات

عندما يتم تعيين هذه الخاصية على`حقيقي` يتم تصدير بيانات الصور مباشرة إلى**صورة** لا يتم إنشاء عناصر وملفات منفصلة.

## أمثلة

يوضح كيفية تضمين الخطوط داخل مستند HTML المحفوظ.

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
