---
title: PclSaveOptions.FallbackFontName
linktitle: FallbackFontName
articleTitle: FallbackFontName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PclSaveOptions FallbackFontName، التي تضمن الطباعة بسلاسة باستخدام الخط الافتراضي عندما لا يكون الخط المطلوب متاحًا.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/pclsaveoptions/fallbackfontname/
---
## PclSaveOptions.FallbackFontName property

اسم الخط الذي سيتم استخدامه إذا لم يتم العثور على الخط المتوقع في الطابعة ومجموعات الخطوط المضمنة.

```csharp
public string FallbackFontName { get; set; }
```

## ملاحظات

إذا لم يتم العثور على خيار بديل، يتم إنشاء تحذير ويتم استخدام الخط "Arial".

## أمثلة

يوضح كيفية إعلان الخط الذي ستطبقه الطابعة على النص المطبوع كبديل في حالة عدم توفر الخط الأصلي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.FallbackFontName = "Times New Roman";

// ستطلب هذه الوثيقة من الطابعة تطبيق خط "Times New Roman" على النص الذي يحتوي على الخط المفقود.
// إذا لم يكن الخط "Times New Roman" متاحًا أيضًا، فسوف تستخدم الطابعة الخط "Arial" افتراضيًا.
doc.Save(ArtifactsDir + "PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

### أنظر أيضا

* class [PclSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
