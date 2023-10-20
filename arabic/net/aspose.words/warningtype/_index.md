---
title: WarningType Enum
linktitle: WarningType
articleTitle: WarningType
second_title: Aspose.Words لـ .NET
description: Aspose.Words.WarningType تعداد. يحدد نوع التحذير الذي يصدره Aspose.Words أثناء تحميل المستند أو حفظه في C#.
type: docs
weight: 6660
url: /ar/net/aspose.words/warningtype/
---
## WarningType enumeration

يحدد نوع التحذير الذي يصدره Aspose.Words أثناء تحميل المستند أو حفظه.

```csharp
[Flags]
public enum WarningType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| DataLossCategory | `FF` | سيتم فقدان بعض النص/الحرف/الصورة أو البيانات الأخرى إما من شجرة المستند بعد التحميل، أو من المستند الذي تم إنشاؤه بعد الحفظ. |
| DataLoss | `1` | فقدان بيانات عام، لا يوجد رمز محدد. |
| MajorFormattingLossCategory | `FF00` | قد يبدو المستند الناتج أو موقع معين فيه مختلفًا إلى حد كبير مقارنة بالمستند الأصلي. |
| MajorFormattingLoss | `100` | فقدان التنسيق الرئيسي العام، لا يوجد رمز محدد. |
| MinorFormattingLossCategory | `FF0000` | قد يبدو المستند الناتج أو موقع معين فيه مختلفًا بعض الشيء مقارنة بالمستند الأصلي. |
| MinorFormattingLoss | `10000` | فقدان تنسيق بسيط عام، لا يوجد رمز محدد. |
| FontSubstitution | `20000` | تم استبدال الخط. |
| FontEmbedding | `40000` | فقدان معلومات الخط المضمنة أثناء حفظ المستند. |
| UnexpectedContentCategory | `F000000` | لا يمكن التعرف على بعض المحتوى الموجود في المستند المصدر (على سبيل المثال، غير مدعوم)، وقد يتسبب هذا أو لا في حدوث مشكلات أو يؤدي إلى فقدان البيانات/التنسيق. |
| UnexpectedContent | `1000000` | محتوى عام غير متوقع، بدون رمز محدد. |
| Hint | `10000000` | ينصح بوجود مشكلة محتملة أو يقترح تحسينًا. |

## أمثلة

يوضح كيفية تعيين الخاصية للعثور على أقرب تطابق لخط مفقود من مصادر الخطوط المتوفرة.

```csharp
public void EnableFontSubstitution()
{
    // افتح مستندًا يحتوي على نص منسق بخط غير موجود في أي من مصادر الخطوط لدينا.
    Document doc = new Document(MyDir + "Missing font.docx");

    // قم بتعيين رد اتصال للتعامل مع تحذيرات استبدال الخط.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // قم بتعيين اسم الخط الافتراضي وتمكين استبدال الخط.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // يجب استخدام مقاييس الخط الأصلي بعد استبدال الخط.
    doc.LayoutOptions.KeepOriginalFontMetrics = true;

    // سنتلقى تحذيرًا بشأن استبدال الخط إذا قمنا بحفظ مستند بخط مفقود.
    doc.FontSettings = fontSettings;
    doc.Save(ArtifactsDir + "FontSettings.EnableFontSubstitution.pdf");

    using (IEnumerator<WarningInfo> warnings = substitutionWarningHandler.FontWarnings.GetEnumerator())
        while (warnings.MoveNext())
            Console.WriteLine(warnings.Current.Description);

    // يمكننا أيضًا التحقق من التحذيرات في المجموعة ومسحها.
    Assert.AreEqual(WarningSource.Layout, substitutionWarningHandler.FontWarnings[0].Source);
    Assert.AreEqual(
        "Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
        substitutionWarningHandler.FontWarnings[0].Description);

    substitutionWarningHandler.FontWarnings.Clear();

    Assert.That(substitutionWarningHandler.FontWarnings, Is.Empty);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// يتم الاتصال به في كل مرة يحدث فيها تحذير أثناء التحميل/الحفظ.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontWarnings.Warning(info);
    }

    public WarningInfoCollection FontWarnings = new WarningInfoCollection();
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
