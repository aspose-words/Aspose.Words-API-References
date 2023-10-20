---
title: Font.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words لـ .NET
description: Font Underline ملكية. الحصول على أو تعيين نوع التسطير المطبق على الخط في C#.
type: docs
weight: 530
url: /ar/net/aspose.words/font/underline/
---
## Font.Underline property

الحصول على أو تعيين نوع التسطير المطبق على الخط.

```csharp
public Underline Underline { get; set; }
```

## أمثلة

يوضح كيفية تكوين نمط ولون التسطير في النص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Underline = Underline.Dotted;
builder.Font.UnderlineColor = Color.Red;

builder.Writeln("Underlined text.");

doc.Save(ArtifactsDir + "Font.Underlines.docx");
```

يوضح كيفية إدراج نص منسق باستخدام DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// حدد تنسيق الخط، ثم أضف النص.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

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

* enum [Underline](../../underline/)
* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
