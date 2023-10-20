---
title: PclSaveOptions.FallbackFontName
linktitle: FallbackFontName
articleTitle: FallbackFontName
second_title: Aspose.Words لـ .NET
description: PclSaveOptions FallbackFontName ملكية. اسم الخط الذي سيتم استخدامه إذا لم يتم العثور على خط متوقع في الطابعة ومجموعات الخطوط المضمنة في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/pclsaveoptions/fallbackfontname/
---
## PclSaveOptions.FallbackFontName property

اسم الخط الذي سيتم استخدامه إذا لم يتم العثور على خط متوقع في الطابعة ومجموعات الخطوط المضمنة.

```csharp
public string FallbackFontName { get; set; }
```

## ملاحظات

إذا لم يتم العثور على أي بديل، فسيتم إنشاء تحذير ويتم استخدام الخط "Arial".

## أمثلة

يوضح كيفية الإعلان عن الخط الذي ستطبقه الطابعة على النص المطبوع كبديل في حالة عدم توفر الخط الأصلي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.FallbackFontName = "Times New Roman";

// سيوجه هذا المستند الطابعة لتطبيق "Times New Roman" على النص الذي يحتوي على الخط المفقود.
// في حالة عدم توفر "Times New Roman" أيضًا، ستستخدم الطابعة الخط "Arial" بشكل افتراضي.
doc.Save(ArtifactsDir + "PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

### أنظر أيضا

* class [PclSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
