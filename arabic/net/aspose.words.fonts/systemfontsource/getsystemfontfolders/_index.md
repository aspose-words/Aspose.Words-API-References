---
title: SystemFontSource.GetSystemFontFolders
linktitle: GetSystemFontFolders
articleTitle: GetSystemFontFolders
second_title: Aspose.Words لـ .NET
description: SystemFontSource GetSystemFontFolders طريقة. إرجاع مجلدات خطوط النظام أو المصفوفة الفارغة إذا لم يكن من الممكن الوصول إلى المجلدات في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.fonts/systemfontsource/getsystemfontfolders/
---
## SystemFontSource.GetSystemFontFolders method

إرجاع مجلدات خطوط النظام أو المصفوفة الفارغة إذا لم يكن من الممكن الوصول إلى المجلدات.

```csharp
public static string[] GetSystemFontFolders()
```

## ملاحظات

في بعض الأنظمة الأساسية، يمكن لـ Aspose.Words البحث في خطوط النظام ليس فقط من خلال المجلدات ولكن في المصادر الأخرى أيضًا. على سبيل المثال، في نظام التشغيل Windows Platform Aspose.Words، ابحث عن الخطوط أيضًا في السجل.

## أمثلة

يوضح كيفية الوصول إلى مصدر خط نظام المستند وتعيين بدائل الخطوط.

```csharp
Document doc = new Document();
doc.FontSettings = new FontSettings();

// بشكل افتراضي، يحتوي المستند الفارغ دائمًا على مصدر خط النظام.
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

// قم بتعيين خط موجود في دليل خطوط Windows كبديل للخط غير الموجود.
doc.FontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;
doc.FontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Kreon-Regular", new[] {"Calibri"});

Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.Contains("Calibri",
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").ToArray());

// بدلاً من ذلك، يمكننا إضافة مصدر خط المجلد حيث يحتوي المجلد المقابل على الخط.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
doc.FontSettings.SetFontsSources(new FontSourceBase[] {systemFontSource, folderFontSource});
Assert.AreEqual(2, doc.FontSettings.GetFontsSources().Length);

// إعادة تعيين مصادر الخطوط لا تزال تتركنا مع مصدر خط النظام بالإضافة إلى البدائل.
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
```

### أنظر أيضا

* class [SystemFontSource](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
