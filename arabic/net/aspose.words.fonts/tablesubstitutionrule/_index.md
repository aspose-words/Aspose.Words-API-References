---
title: Class TableSubstitutionRule
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fonts.TableSubstitutionRule فصل. قاعدة استبدال خط الجدول .
type: docs
weight: 2880
url: /ar/net/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class

قاعدة استبدال خط الجدول .

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
| [AddSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/addsubstitutes/)(string, params string[]) | يضيف أسماء خطوط بديلة لاسم الخط الأصلي المحدد. |
| [GetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/getsubstitutes/)(string) | إرجاع مصفوفة تحتوي على أسماء خطوط بديلة لاسم الخط الأصلي المحدد. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load)(Stream) | تحميل إعدادات استبدال الجدول من دفق XML . |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load_1)(string) | تحميل إعدادات استبدال الجدول من ملف XML . |
| [LoadAndroidSettings](../../aspose.words.fonts/tablesubstitutionrule/loadandroidsettings/)() | تحميل إعدادات استبدال الجدول المحددة مسبقًا لمنصة Linux. |
| [LoadLinuxSettings](../../aspose.words.fonts/tablesubstitutionrule/loadlinuxsettings/)() | تحميل إعدادات استبدال الجدول المحددة مسبقًا لمنصة Linux. |
| [LoadWindowsSettings](../../aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/)() | تحميل إعدادات استبدال الجدول المحددة مسبقًا لمنصة Windows. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save)(Stream) | يحفظ إعدادات استبدال الجدول الحالية للدفق. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save_1)(string) | يحفظ إعدادات الاستبدال الحالية للجدول في ملف. |
| [SetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/setsubstitutes/)(string, params string[]) | تجاوز أسماء الخطوط البديلة لاسم الخط الأصلي المحدد. |

### ملاحظات

تحدد هذه القاعدة قائمة أسماء الخطوط البديلة التي سيتم استخدامها في حالة عدم توفر الخط الأصلي. سيتم التحقق من البدائل لاسم الخط و[`AltName`](../fontinfo/altname/) (إن وجد) .

### أمثلة

يوضح كيفية الوصول إلى جداول استبدال الخطوط لنظامي التشغيل Windows و Linux.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// قم بإنشاء قاعدة استبدال جديدة للجدول وقم بتحميل جدول استبدال خطوط Microsoft Windows الافتراضي.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// في Windows ، البديل الافتراضي لخط "Times New Roman CE" هو "Times New Roman".
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// يمكننا حفظ الجدول في شكل وثيقة XML.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// لينكس لديه جدول الاستبدال الخاص به.
// هناك عدة خطوط بديلة لـ "Times New Roman CE".
// إذا كان البديل الأول "FreeSerif" غير متوفر أيضًا ،
// ستنتقل هذه القاعدة بين الآخرين في المصفوفة حتى تجد قاعدة متاحة.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// احفظ جدول استبدال Linux في شكل مستند XML باستخدام التدفق.
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


