---
title: TableSubstitutionRule.SetSubstitutes
second_title: Aspose.Words لمراجع .NET API
description: TableSubstitutionRule طريقة. تجاوز أسماء الخطوط البديلة لاسم الخط الأصلي المحدد.
type: docs
weight: 80
url: /ar/net/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule.SetSubstitutes method

تجاوز أسماء الخطوط البديلة لاسم الخط الأصلي المحدد.

```csharp
public void SetSubstitutes(string originalFontName, params string[] substituteFontNames)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| originalFontName | String | اسم الخط الأصلي. |
| substituteFontNames | String[] | قائمة أسماء الخطوط البديلة. |

### أمثلة

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

يوضح كيفية العمل مع جداول استبدال الخطوط المخصصة.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// أنشئ قاعدة استبدال جدول جديدة وقم بتحميل جدول استبدال خطوط Windows الافتراضي.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// إذا اخترنا الخطوط حصريًا من مجلدنا، فسنحتاج إلى جدول استبدال مخصص.
// لن نتمكن بعد الآن من الوصول إلى خطوط Microsoft Windows،
// مثل "Arial" أو "Times New Roman" لأنها غير موجودة في مجلد الخطوط الجديد.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// فيما يلي طريقتان لتحميل جدول بديل من ملف في نظام الملفات المحلي.
// 1 - من الدفق:
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - مباشرة من ملف:
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// نظرًا لأنه لم يعد بإمكاننا الوصول إلى "Arial"، سيحاول جدول الخطوط الخاص بنا أولاً استبداله بـ "Nonexistent Font".
// ليس لدينا هذا الخط بحيث سيتم نقله إلى البديل التالي، "Kreon"، الموجود في المجلد "MyFonts".
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// يمكننا توسيع هذا الجدول برمجياً. سوف نقوم بإضافة إدخال يستبدل "Times New Roman" بـ "Arvo"
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// يمكننا إضافة بديل احتياطي ثانوي لإدخال خط موجود باستخدام AddSubstitutes().
// في حالة عدم توفر "Arvo"، سيبحث جدولنا عن "M+ 2m" كخيار بديل ثانٍ.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// يمكن لـ SetSubstitutes() تعيين قائمة جديدة من الخطوط البديلة للخط.
tableSubstitutionRule.SetSubstitutes("Times New Roman", new[] {"Squarish Sans CT", "M+ 2m"});
Assert.AreEqual(new[] {"Squarish Sans CT", "M+ 2m"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// ستؤدي كتابة النص بالخطوط التي لا يمكننا الوصول إليها إلى استدعاء قواعد الاستبدال الخاصة بنا.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial";
builder.Writeln("Text written in Arial, to be substituted by Kreon.");

builder.Font.Name = "Times New Roman";
builder.Writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Custom.pdf");
```

### أنظر أيضا

* class [TableSubstitutionRule](../)
* مساحة الاسم [Aspose.Words.Fonts](../../tablesubstitutionrule/)
* المجسم [Aspose.Words](../../../)


