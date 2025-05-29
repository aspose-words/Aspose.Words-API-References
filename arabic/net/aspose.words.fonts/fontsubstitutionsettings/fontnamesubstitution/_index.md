---
title: FontSubstitutionSettings.FontNameSubstitution
linktitle: FontNameSubstitution
articleTitle: FontNameSubstitution
second_title: Aspose.Words لـ .NET
description: حسّن أسلوب طباعتك باستخدام FontSubstitutionSettings. اكتشف كيفية تخصيص قواعد أسماء الخطوط لتحسين مرونة التصميم وتجربة المستخدم.
type: docs
weight: 40
url: /ar/net/aspose.words.fonts/fontsubstitutionsettings/fontnamesubstitution/
---
## FontSubstitutionSettings.FontNameSubstitution property

الإعدادات المتعلقة بقاعدة استبدال اسم الخط.

```csharp
public FontNameSubstitutionRule FontNameSubstitution { get; }
```

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

### أنظر أيضا

* class [FontNameSubstitutionRule](../../fontnamesubstitutionrule/)
* class [FontSubstitutionSettings](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
