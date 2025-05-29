---
title: HtmlSaveOptions.ExportFontsAsBase64
linktitle: ExportFontsAsBase64
articleTitle: ExportFontsAsBase64
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية HtmlSaveOptions ExportFontsAsBase64 لغة HTML لديك من خلال تضمين الخطوط بترميز Base64 لتحسين الأداء. افتراضيًا، خطأ.
type: docs
weight: 150
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportfontsasbase64/
---
## HtmlSaveOptions.ExportFontsAsBase64 property

يحدد ما إذا كان يجب تضمين موارد الخطوط في HTML بترميز Base64. الافتراضي هو`خطأ شنيع` .

```csharp
public bool ExportFontsAsBase64 { get; set; }
```

## ملاحظات

افتراضيًا، تُكتب الخطوط في ملفات منفصلة. إذا تم ضبط هذا الخيار على`حقيقي`سيتم تضمين الخطوط في CSS الخاص بالمستند باستخدام ترميز Base64.

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
