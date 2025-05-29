---
title: Document.FontSettings
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية تخصيص إعدادات خطوط المستندات بسهولة. حسّن مستنداتك بخيارات خطوط مُخصصة لتحسين سهولة القراءة والأسلوب.
type: docs
weight: 150
url: /ar/net/aspose.words/document/fontsettings/
---
## Document.FontSettings property

يحصل على إعدادات خط المستند أو يعينها.

```csharp
public FontSettings FontSettings { get; set; }
```

## ملاحظات

تسمح هذه الخاصية بتحديد إعدادات الخط لكل مستند. إذا تم ضبطها على`باطل` ، إعدادات الخط الثابت الافتراضية [`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) سيتم استخدامها.

القيمة الافتراضية هي`باطل`.

## أمثلة

يوضح كيفية تعيين قواعد استبدال الخط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

//تحتوي مصادر الخط الافتراضية على الخط الأول الذي تستخدمه المستند.
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// الخط الثاني "Amethysta" غير متوفر.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// يمكننا تكوين جدول استبدال الخط الذي يحدد
// ما هي الخطوط التي سيستخدمها Aspose.Words كبدائل للخطوط غير المتوفرة.
// تعيين خطين بديلين لـ "Amethysta": "Arvo"، و"Courier New".
// إذا كان البديل الأول غير متاح، يحاول Aspose.Words استخدام البديل الثاني، وهكذا.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // "Amethysta" غير متوفر، وقاعدة الاستبدال تنص على أن الخط الأول الذي يجب استخدامه كبديل هو "Arvo".
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 // "Arvo" غير متوفر أيضًا، ولكن "Courier New" متوفر.
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// ستعرض وثيقة الإخراج النص الذي يستخدم الخط "Amethysta" بتنسيق "Courier New".
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

### أنظر أيضا

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
