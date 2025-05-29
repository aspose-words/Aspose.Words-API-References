---
title: Underline Enum
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Underline enum لخيارات تسطير الخطوط المتنوعة. حسّن تنسيق مستنداتك بأنماط قابلة للتخصيص اليوم!
type: docs
weight: 7360
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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
