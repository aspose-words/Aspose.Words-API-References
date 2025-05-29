---
title: TableSubstitutionRule.AddSubstitutes
linktitle: AddSubstitutes
articleTitle: AddSubstitutes
second_title: Aspose.Words لـ .NET
description: قم بتعزيز أسلوب الطباعة لديك باستخدام طريقة AddSubstitutes في TableSubstitutionRule، مما يسمح بالتكامل السلس للخطوط البديلة لأي خط أصلي.
type: docs
weight: 10
url: /ar/net/aspose.words.fonts/tablesubstitutionrule/addsubstitutes/
---
## TableSubstitutionRule.AddSubstitutes method

يضيف أسماء الخطوط البديلة لاسم الخط الأصلي المحدد.

```csharp
public void AddSubstitutes(string originalFontName, params string[] substituteFontNames)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| originalFontName | String | اسم الخط الأصلي. |
| substituteFontNames | String[] | قائمة أسماء الخطوط البديلة. |

## أمثلة

يوضح كيفية الوصول إلى مصدر الخط الخاص بنظام المستند وتعيين بدائل الخط.

```csharp
Document doc = new Document();
doc.FontSettings = new FontSettings();

// بشكل افتراضي، تحتوي المستندة الفارغة دائمًا على مصدر خط النظام.
Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);

SystemFontSource systemFontSource = (SystemFontSource) doc.FontSettings.GetFontsSources()[0];
Assert.AreEqual(FontSourceType.SystemFonts, systemFontSource.Type);
Assert.AreEqual(0, systemFontSource.Priority);

PlatformID pid = Environment.OSVersion.Platform;
bool isWindows = (pid == PlatformID.Win32NT) || (pid == PlatformID.Win32S) ||
                 (pid == PlatformID.Win32Windows) || (pid == PlatformID.WinCE);
if (isWindows)
{
    const string fontsPath = @"C:\WINDOWS\Fonts";
    Assert.AreEqual(fontsPath.ToLower(),
        SystemFontSource.GetSystemFontFolders().FirstOrDefault()?.ToLower());
}

foreach (string systemFontFolder in SystemFontSource.GetSystemFontFolders())
{
    Console.WriteLine(systemFontFolder);
}

// تعيين الخط الموجود في دليل خطوط Windows كبديل للخط غير الموجود.
doc.FontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;
doc.FontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Kreon-Regular", new[] {"Calibri"});

Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.Contains("Calibri",
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").ToArray());

//بدلاً من ذلك، يمكننا إضافة مصدر خط المجلد الذي يحتوي على الخط المقابل.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
doc.FontSettings.SetFontsSources(new FontSourceBase[] {systemFontSource, folderFontSource});
Assert.AreEqual(2, doc.FontSettings.GetFontsSources().Length);

// إعادة تعيين مصادر الخط لا يزال يترك لنا مصدر الخط الخاص بالنظام بالإضافة إلى البدائل لدينا.
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.True(doc.FontSettings.SubstitutionSettings.FontNameSubstitution.Enabled);
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
