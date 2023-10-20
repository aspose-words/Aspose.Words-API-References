---
title: Font.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words لـ .NET
description: Font ClearFormatting طريقة. إعادة التعيين إلى تنسيق الخط الافتراضي في C#.
type: docs
weight: 550
url: /ar/net/aspose.words/font/clearformatting/
---
## Font.ClearFormatting method

إعادة التعيين إلى تنسيق الخط الافتراضي.

```csharp
public void ClearFormatting()
```

## ملاحظات

إزالة كافة تنسيقات الخطوط المحددة صراحةً في الكائن الذي منه[`Font`](../) تم الحصول عليه لذا سيتم توريث تنسيق الخط من الأصل المناسب.

## أمثلة

يوضح كيفية إدراج حقل الارتباط التشعبي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// أدخل ارتباطًا تشعبيًا وقم بإبرازه بتنسيق مخصص.
// سيكون الارتباط التشعبي عبارة عن جزء من النص قابل للنقر عليه والذي سينقلنا إلى الموقع المحدد في عنوان URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com"، خطأ);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + النقر بزر الماوس الأيسر على الرابط الموجود في النص في Microsoft Word سينقلنا إلى عنوان URL عبر نافذة متصفح ويب جديدة.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
