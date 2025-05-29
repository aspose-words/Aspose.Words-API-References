---
title: Font.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "تسطير الخط" لتخصيص أنماط النص. حدّد أنواع التسطير وعدّلها بسهولة لتحسين جودة الطباعة في تصاميمك.
type: docs
weight: 540
url: /ar/net/aspose.words/font/underline/
---
## Font.Underline property

يحصل على نوع الخط السفلي المطبق على الخط أو يعينه.

```csharp
public Underline Underline { get; set; }
```

## أمثلة

يوضح كيفية تكوين نمط ولون تسطير النص.

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

يوضح كيفية إدراج حقل ارتباط تشعبي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

//أدرج ارتباطًا تشعبيًا وأبرزه باستخدام التنسيق المخصص.
// سيكون الرابط التشعبي عبارة عن جزء نصي قابل للنقر والذي سيأخذنا إلى الموقع المحدد في عنوان URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com"، خطأ);
builder.Font.ClearFormatting();
builder.Writeln(".");

// الضغط على Ctrl + النقر بزر الماوس الأيسر على الرابط الموجود في النص في Microsoft Word سيأخذنا إلى عنوان URL عبر نافذة متصفح ويب جديدة.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### أنظر أيضا

* enum [Underline](../../underline/)
* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
