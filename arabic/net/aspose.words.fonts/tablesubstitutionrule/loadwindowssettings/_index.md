---
title: TableSubstitutionRule.LoadWindowsSettings
second_title: Aspose.Words لمراجع .NET API
description: TableSubstitutionRule طريقة. يقوم بتحميل إعدادات استبدال الجدول المحددة مسبقًا لنظام التشغيل Windows.
type: docs
weight: 60
url: /ar/net/aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/
---
## TableSubstitutionRule.LoadWindowsSettings method

يقوم بتحميل إعدادات استبدال الجدول المحددة مسبقًا لنظام التشغيل Windows.

```csharp
public void LoadWindowsSettings()
```

### أمثلة

يوضح كيفية الوصول إلى جداول استبدال الخطوط لنظامي التشغيل Windows وLinux.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// أنشئ قاعدة استبدال جدول جديدة وقم بتحميل جدول استبدال الخطوط الافتراضي لـ Microsoft Windows.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// في نظام التشغيل Windows، البديل الافتراضي للخط "Times New Roman CE" هو "Times New Roman".
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// يمكننا حفظ الجدول في شكل مستند XML.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// Linux لديه جدول استبدال خاص به.
// هناك خطوط بديلة متعددة لـ "Times New Roman CE".
// إذا كان البديل الأول، "FreeSerif" غير متاح أيضًا،
// ستنتقل هذه القاعدة عبر القواعد الأخرى في المصفوفة حتى تجد قاعدة متاحة.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// احفظ جدول استبدال Linux في شكل مستند XML باستخدام الدفق.
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### أنظر أيضا

* class [TableSubstitutionRule](../)
* مساحة الاسم [Aspose.Words.Fonts](../../tablesubstitutionrule/)
* المجسم [Aspose.Words](../../../)


