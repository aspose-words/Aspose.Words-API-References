---
title: Underline Enum
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Underline تعداد. يشير إلى نوع التسطير المطبق على الخط في C#.
type: docs
weight: 6510
url: /ar/net/aspose.words/underline/
---
## Underline enumeration

يشير إلى نوع التسطير المطبق على الخط.

```csharp
public enum Underline
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` |  |
| Single | `1` |  |
| Words | `2` |  |
| Double | `3` |  |
| Dotted | `4` |  |
| Thick | `6` |  |
| Dash | `7` |  |
| DashLong | `39` |  |
| DotDash | `9` |  |
| DotDotDash | `10` |  |
| Wavy | `11` |  |
| DottedHeavy | `20` |  |
| DashHeavy | `23` |  |
| DashLongHeavy | `55` |  |
| DotDashHeavy | `25` |  |
| DotDotDashHeavy | `26` |  |
| WavyHeavy | `27` |  |
| WavyDouble | `43` |  |

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
