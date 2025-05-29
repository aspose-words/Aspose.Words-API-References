---
title: TableSubstitutionRule Class
linktitle: TableSubstitutionRule
articleTitle: TableSubstitutionRule
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fonts.TableSubstitutionRule لإدارة الخطوط بكفاءة وتنسيق النصوص بسلاسة في مستنداتك.
type: docs
weight: 3490
url: /ar/net/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class

قاعدة استبدال خط الجدول.

لمعرفة المزيد، قم بزيارة[العمل مع الخطوط](https://docs.aspose.com/words/net/working-with-fonts/) مقالة توثيقية.

```csharp
public class TableSubstitutionRule : FontSubstitutionRule
```

## الخصائص

| اسم | وصف |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | يحدد ما إذا كانت القاعدة ممكّنة أم لا. |

## طُرق

| اسم | وصف |
| --- | --- |
| [AddSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/addsubstitutes/)(*string, params string[]*) | يضيف أسماء الخطوط البديلة لاسم الخط الأصلي المحدد. |
| [GetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/getsubstitutes/)(*string*) | إرجاع المصفوفة التي تحتوي على أسماء الخطوط البديلة لاسم الخط الأصلي المحدد. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load)(*Stream*) | يقوم بتحميل إعدادات استبدال الجدول من دفق XML. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load_1)(*string*) | يقوم بتحميل إعدادات استبدال الجدول من ملف XML. |
| [LoadAndroidSettings](../../aspose.words.fonts/tablesubstitutionrule/loadandroidsettings/)() | يقوم بتحميل إعدادات استبدال الجدول المحددة مسبقًا لمنصة Android. |
| [LoadLinuxSettings](../../aspose.words.fonts/tablesubstitutionrule/loadlinuxsettings/)() | يقوم بتحميل إعدادات استبدال الجدول المحددة مسبقًا لمنصة Linux. |
| [LoadWindowsSettings](../../aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/)() | يقوم بتحميل إعدادات استبدال الجدول المحددة مسبقًا لمنصة Windows. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save)(*Stream*) | يحفظ إعدادات استبدال الجدول الحالية إلى stream. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save_1)(*string*) | يحفظ إعدادات استبدال الجدول الحالية في الملف. |
| [SetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/setsubstitutes/)(*string, params string[]*) | تجاوز أسماء الخطوط البديلة لاسم الخط الأصلي المحدد. |

## ملاحظات

تحدد هذه القاعدة قائمة أسماء الخطوط البديلة التي سيتم استخدامها إذا لم يكن الخط الأصلي متاحًا. سيتم التحقق من البدائل لمعرفة اسم الخط و[`AltName`](../fontinfo/altname/) (إن وجد).

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

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
