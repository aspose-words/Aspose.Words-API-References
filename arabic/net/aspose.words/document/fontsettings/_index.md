---
title: Document.FontSettings
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words لـ .NET
description: Document FontSettings ملكية. الحصول على إعدادات خط المستند أو تعيينها في C#.
type: docs
weight: 140
url: /ar/net/aspose.words/document/fontsettings/
---
## Document.FontSettings property

الحصول على إعدادات خط المستند أو تعيينها.

```csharp
public FontSettings FontSettings { get; set; }
```

## ملاحظات

تسمح هذه الخاصية بتحديد إعدادات الخط لكل مستند. إذا تم تعيينه على`باطل` إعدادات الخط الثابت الافتراضي [`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) سوف يستخدم.

القيمة الافتراضية هي`باطل`.

## أمثلة

يوضح كيفية ضبط قواعد استبدال الخط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// تحتوي مصادر الخطوط الافتراضية على الخط الأول الذي يستخدمه المستند.
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// الخط الثاني، "Amethysta"، غير متوفر.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// يمكننا تكوين جدول استبدال الخطوط الذي يحدد
// الخطوط التي سيستخدمها Aspose.Words كبدائل للخطوط غير المتوفرة.
// قم بتعيين خطين بديلين لـ "Amethysta": "Arvo" و"Courier New".
// إذا كان البديل الأول غير متاح، يحاول Aspose.Words استخدام البديل الثاني، وهكذا.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // "Amethysta" غير متاح، وتنص قاعدة الاستبدال على أن الخط الأول الذي سيتم استخدامه كبديل هو "Arvo".
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 // "Arvo" غير متاح أيضًا، ولكن "Courier New" متاح أيضًا.
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// سيعرض مستند الإخراج النص الذي يستخدم الخط "Amethysta" المنسق باستخدام "Courier New".
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

### أنظر أيضا

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
