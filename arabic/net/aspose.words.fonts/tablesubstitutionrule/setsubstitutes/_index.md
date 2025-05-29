---
title: TableSubstitutionRule.SetSubstitutes
linktitle: SetSubstitutes
articleTitle: SetSubstitutes
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية تخصيص أسماء الخطوط باستخدام طريقة TableSubstitutionRule SetSubstitutes. حسّن تصميمك بحلول طباعة مُخصصة!
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

يوضح كيفية العمل مع جداول استبدال الخطوط المخصصة.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// قم بإنشاء قاعدة استبدال جدول جديدة وتحميل جدول استبدال الخطوط الافتراضي لنظام التشغيل Windows.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// إذا قمنا باختيار الخطوط من مجلدنا حصريًا، فسنحتاج إلى جدول استبدال مخصص.
// لن نتمكن بعد الآن من الوصول إلى خطوط Microsoft Windows،
// مثل "Arial" أو "Times New Roman" لأنها غير موجودة في مجلد الخط الجديد لدينا.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// فيما يلي طريقتان لتحميل جدول الاستبدال من ملف في نظام الملفات المحلي.
// 1 - من مجرى:
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - مباشرة من الملف:
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// نظرًا لأنه لم يعد لدينا إمكانية الوصول إلى "Arial"، فإن جدول الخطوط لدينا سيحاول أولاً استبداله بـ "Nonexistent Font".
// ليس لدينا هذا الخط حتى نتمكن من الانتقال إلى البديل التالي، "Kreon"، الموجود في مجلد "MyFonts".
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// يمكننا توسيع هذا الجدول برمجيًا. سنضيف مدخلًا يستبدل "Times New Roman" بـ "Arvo".
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// يمكننا إضافة بديل احتياطي ثانوي لإدخال خط موجود باستخدام AddSubstitutes().
// في حالة عدم توفر "Arvo"، سيبحث جدولنا عن "M+ 2m" كخيار بديل ثانٍ.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// يمكن لـ SetSubstitutes() تعيين قائمة جديدة من الخطوط البديلة لخط ما.
tableSubstitutionRule.SetSubstitutes("Times New Roman", "Squarish Sans CT", "M+ 2m");
Assert.AreEqual(new[] {"Squarish Sans CT", "M+ 2m"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// كتابة النص في الخطوط التي لا نستطيع الوصول إليها سوف يستدعي قواعد الاستبدال الخاصة بنا.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial";
builder.Writeln("Text written in Arial, to be substituted by Kreon.");

builder.Font.Name = "Times New Roman";
builder.Writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Custom.pdf");
```

### أنظر أيضا

* class [TableSubstitutionRule](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
