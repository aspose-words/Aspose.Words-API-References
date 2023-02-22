---
title: Font.Color
second_title: Aspose.Words لمراجع .NET API
description: Font ملكية. الحصول على لون الخط أو تحديده.
type: docs
weight: 70
url: /ar/net/aspose.words/font/color/
---
## Font.Color property

الحصول على لون الخط أو تحديده.

```csharp
public Color Color { get; set; }
```

### أمثلة

يوضح كيفية إدراج نص منسق باستخدام DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// حدد تنسيق الخط ، ثم أضف نصًا.
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

// أدخل ارتباطًا تشعبيًا وقم بتأكيده بتنسيق مخصص.
// سيكون الارتباط التشعبي عبارة عن نص قابل للنقر عليه والذي سينقلنا إلى الموقع المحدد في عنوان URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com "، خطأ) ;
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + النقر على الرابط الأيسر في النص في Microsoft Word سينقلنا إلى عنوان URL عبر نافذة متصفح ويب جديدة.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../font/)
* المجسم [Aspose.Words](../../../)


