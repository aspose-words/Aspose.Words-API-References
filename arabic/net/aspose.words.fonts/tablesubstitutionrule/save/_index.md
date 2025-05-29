---
title: TableSubstitutionRule.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words لـ .NET
description: احفظ إعدادات استبدال جدولك بسهولة باستخدام طريقة حفظ TableSubstitutionRule. بسّط إدارة بياناتك اليوم!
type: docs
weight: 70
url: /ar/net/aspose.words.fonts/tablesubstitutionrule/save/
---
## Save(*string*) {#save_1}

يحفظ إعدادات استبدال الجدول الحالية في الملف.

```csharp
public void Save(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم ملف الإخراج. |

## أمثلة

يوضح كيفية الوصول إلى جداول استبدال الخطوط لنظامي التشغيل Windows وLinux.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// قم بإنشاء قاعدة استبدال جدول جديدة وتحميل جدول استبدال الخطوط الافتراضي لنظام التشغيل Microsoft Windows.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// في Windows، البديل الافتراضي للخط "Times New Roman CE" هو "Times New Roman".
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

//يمكننا حفظ الجدول في شكل مستند XML.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

//يحتوي Linux على جدول الاستبدال الخاص به.
// هناك عدة خطوط بديلة لـ "Times New Roman CE".
// إذا كان البديل الأول، "FreeSerif"، غير متاح أيضًا،
// ستقوم هذه القاعدة بالتنقل بين القواعد الأخرى في المصفوفة حتى تجد قاعدة متاحة.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// احفظ جدول الاستبدال الخاص بنظام Linux في شكل مستند XML باستخدام دفق.
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### أنظر أيضا

* class [TableSubstitutionRule](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)

---

## Save(*Stream*) {#save}

يحفظ إعدادات استبدال الجدول الحالية إلى stream.

```csharp
public void Save(Stream outputStream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| outputStream | Stream | تيار الإخراج. |

## أمثلة

يوضح كيفية الوصول إلى جداول استبدال الخطوط لنظامي التشغيل Windows وLinux.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// قم بإنشاء قاعدة استبدال جدول جديدة وتحميل جدول استبدال الخطوط الافتراضي لنظام التشغيل Microsoft Windows.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// في Windows، البديل الافتراضي للخط "Times New Roman CE" هو "Times New Roman".
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

//يمكننا حفظ الجدول في شكل مستند XML.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

//يحتوي Linux على جدول الاستبدال الخاص به.
// هناك عدة خطوط بديلة لـ "Times New Roman CE".
// إذا كان البديل الأول، "FreeSerif"، غير متاح أيضًا،
// ستقوم هذه القاعدة بالتنقل بين القواعد الأخرى في المصفوفة حتى تجد قاعدة متاحة.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// احفظ جدول الاستبدال الخاص بنظام Linux في شكل مستند XML باستخدام دفق.
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### أنظر أيضا

* class [TableSubstitutionRule](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
