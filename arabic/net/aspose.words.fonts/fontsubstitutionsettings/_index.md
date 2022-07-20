---
title: FontSubstitutionSettings
second_title: Aspose.Words لمراجع .NET API
description: يحدد إعدادات آلية استبدال الخط.
type: docs
weight: 2830
url: /ar/net/aspose.words.fonts/fontsubstitutionsettings/
---
## FontSubstitutionSettings class

يحدد إعدادات آلية استبدال الخط.

```csharp
public class FontSubstitutionSettings
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [DefaultFontSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution) { get; } | الإعدادات المتعلقة بقاعدة استبدال الخط الافتراضية. |
| [FontConfigSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontconfigsubstitution) { get; } | الإعدادات المتعلقة بقاعدة استبدال تكوين الخط. |
| [FontInfoSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontinfosubstitution) { get; } | الإعدادات المتعلقة بقاعدة استبدال معلومات الخط. |
| [FontNameSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontnamesubstitution) { get; } | الإعدادات المتعلقة بقاعدة استبدال اسم الخط. |
| [TableSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/tablesubstitution) { get; } | الإعدادات المتعلقة بقاعدة استبدال الجدول ._ x000d_ |

### ملاحظات

تتكون عملية استبدال الخط من عدة قواعد يتم التحقق منها واحدة تلو الأخرى بترتيب معين. إذا لم تتمكن القاعدة الأولى من حل الخط ، فسيتم فحص القاعدة الثانية وهكذا.

ترتيب القواعد هو التالي: 1. قاعدة استبدال اسم الخط (ممكنة افتراضيًا) 2. قاعدة استبدال تكوين الخط (معطلة افتراضيًا) 3. قاعدة استبدال الجدول (ممكنة افتراضيًا) 4. قاعدة استبدال معلومات الخط (ممكّن افتراضيًا) 5. قاعدة الخط الافتراضية (ممكنة افتراضيًا)

لاحظ أن قاعدة استبدال معلومات الخط ستعمل دائمًا على حل الخط إذا كان[`FontInfo`](../fontinfo) هو available وسوف يتجاوز قاعدة الخط الافتراضية. إذا كنت تريد استخدام قاعدة الخط الافتراضية ، فعليك تعطيل قاعدة استبدال معلومات الخط .

لاحظ أن قاعدة استبدال تكوين الخط ستحل الخط في معظم الحالات وبالتالي تتجاوز جميع القواعد الأخرى.

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

* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->