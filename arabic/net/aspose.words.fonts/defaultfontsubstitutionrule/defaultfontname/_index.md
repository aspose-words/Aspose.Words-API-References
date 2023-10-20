---
title: DefaultFontSubstitutionRule.DefaultFontName
linktitle: DefaultFontName
articleTitle: DefaultFontName
second_title: Aspose.Words لـ .NET
description: DefaultFontSubstitutionRule DefaultFontName ملكية. الحصول على اسم الخط الافتراضي أو تعيينه في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/
---
## DefaultFontSubstitutionRule.DefaultFontName property

الحصول على اسم الخط الافتراضي أو تعيينه.

```csharp
public string DefaultFontName { get; set; }
```

## ملاحظات

القيمة الافتراضية هي "تايمز نيو رومان".

## أمثلة

يوضح كيفية تعيين قاعدة استبدال الخط الافتراضية.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// احصل على قاعدة الاستبدال الافتراضية ضمن FontSettings.
// ستستبدل هذه القاعدة كافة الخطوط المفقودة بـ "Times New Roman".
DefaultFontSubstitutionRule defaultFontSubstitutionRule =
    fontSettings.SubstitutionSettings.DefaultFontSubstitution;
Assert.True(defaultFontSubstitutionRule.Enabled);
Assert.AreEqual("Times New Roman", defaultFontSubstitutionRule.DefaultFontName);

// قم بتعيين بديل الخط الافتراضي على "Courier New".
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// باستخدام أداة إنشاء المستندات، أضف بعض النص بخط لا نحتاجه حتى يتم الاستبدال،
// ثم قم بتقديم النتيجة في ملف PDF.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Missing Font";
builder.Writeln("Line written in a missing font, which will be substituted with Courier New.");

doc.Save(ArtifactsDir + "FontSettings.DefaultFontSubstitutionRule.pdf");
```

يوضح كيفية تحديد الخط الافتراضي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// تحتوي مصادر الخطوط التي يستخدمها المستند على الخط "Arial"، وليس "Arvo".
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// قم بتعيين خاصية "DefaultFontName" على "Courier New" لـ،
 // أثناء عرض المستند، قم بتطبيق هذا الخط في جميع الحالات عندما لا يتوفر خط آخر.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// سيستخدم Aspose.Words الآن الخط الافتراضي بدلاً من أي خطوط مفقودة أثناء أي استدعاءات عرض.
doc.Save(ArtifactsDir + "FontSettings.DefaultFontName.pdf");
```

### أنظر أيضا

* class [DefaultFontSubstitutionRule](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
