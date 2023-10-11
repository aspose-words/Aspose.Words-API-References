---
title: Class TableSubstitutionRule
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fonts.TableSubstitutionRule فصل. قاعدة استبدال خط الجدول.
type: docs
weight: 3060
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
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | يحدد ما إذا كانت القاعدة مفعلة أم لا. |

## طُرق

| اسم | وصف |
| --- | --- |
| [AddSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/addsubstitutes/)(string, params string[]) | إضافة أسماء الخطوط البديلة لاسم الخط الأصلي المحدد. |
| [GetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/getsubstitutes/)(string) | إرجاع مصفوفة تحتوي على أسماء خطوط بديلة لاسم الخط الأصلي المحدد. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load)(Stream) | تحميل إعدادات استبدال الجدول من تدفق XML. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load_1)(string) | تحميل إعدادات استبدال الجدول من ملف XML. |
| [LoadAndroidSettings](../../aspose.words.fonts/tablesubstitutionrule/loadandroidsettings/)() | يقوم بتحميل إعدادات استبدال الجدول المحددة مسبقًا لنظام التشغيل Android. |
| [LoadLinuxSettings](../../aspose.words.fonts/tablesubstitutionrule/loadlinuxsettings/)() | تحميل إعدادات استبدال الجدول المحددة مسبقًا لنظام التشغيل Linux. |
| [LoadWindowsSettings](../../aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/)() | يقوم بتحميل إعدادات استبدال الجدول المحددة مسبقًا لنظام التشغيل Windows. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save)(Stream) | يحفظ إعدادات استبدال الجدول الحالية للبث. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save_1)(string) | يحفظ إعدادات استبدال الجدول الحالية في ملف. |
| [SetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/setsubstitutes/)(string, params string[]) | تجاوز أسماء الخطوط البديلة لاسم الخط الأصلي المحدد. |

### ملاحظات

تحدد هذه القاعدة قائمة أسماء الخطوط البديلة التي سيتم استخدامها في حالة عدم توفر الخط الأصلي. سيتم التحقق من البدائل لاسم الخط واسم الخط[`AltName`](../fontinfo/altname/) (إن وجد).

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

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)


