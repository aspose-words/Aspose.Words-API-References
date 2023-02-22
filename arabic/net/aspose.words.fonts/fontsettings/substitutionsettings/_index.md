---
title: FontSettings.SubstitutionSettings
second_title: Aspose.Words لمراجع .NET API
description: FontSettings ملكية. الإعدادات المتعلقة بآلية استبدال الخط.
type: docs
weight: 40
url: /ar/net/aspose.words.fonts/fontsettings/substitutionsettings/
---
## FontSettings.SubstitutionSettings property

الإعدادات المتعلقة بآلية استبدال الخط.

```csharp
public FontSubstitutionSettings SubstitutionSettings { get; }
```

### أمثلة

يوضح كيفية الوصول إلى مصدر خط نظام المستند وتعيين بدائل الخط.

```csharp
Document doc = new Document();
doc.FontSettings = new FontSettings();

// بشكل افتراضي ، يحتوي المستند الفارغ دائمًا على مصدر خط النظام.
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

// تعيين خط موجود في دليل Windows Fonts كبديل لخط غير موجود.
doc.FontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;
doc.FontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Kreon-Regular", new[] {"Calibri"});

Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.Contains("Calibri",
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").ToArray());

// بدلاً من ذلك ، يمكننا إضافة مصدر خط مجلد يحتوي فيه المجلد المقابل على الخط.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
doc.FontSettings.SetFontsSources(new FontSourceBase[] {systemFontSource, folderFontSource});
Assert.AreEqual(2, doc.FontSettings.GetFontsSources().Length);

// لا تزال إعادة تعيين مصادر الخط تترك لنا مصدر خط النظام وكذلك البدائل.
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
```

### أنظر أيضا

* class [FontSubstitutionSettings](../../fontsubstitutionsettings/)
* class [FontSettings](../)
* مساحة الاسم [Aspose.Words.Fonts](../../fontsettings/)
* المجسم [Aspose.Words](../../../)


