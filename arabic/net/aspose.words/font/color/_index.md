---
title: Font.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية لون الخط لتخصيص ألوان النصوص بسهولة في تصميماتك. حسّن سهولة القراءة والجمال بألوان زاهية وجذابة!
type: docs
weight: 70
url: /ar/net/aspose.words/font/color/
---
## Font.Color property

يحصل على لون الخط أو يعينه.

```csharp
public Color Color { get; set; }
```

## أمثلة

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

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
