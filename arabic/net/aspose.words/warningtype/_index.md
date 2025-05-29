---
title: WarningType Enum
linktitle: WarningType
articleTitle: WarningType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.WarningType enum، الذي يصنف التحذيرات أثناء تحميل المستند أو حفظه، مما يعمل على تحسين تجربة إدارة المستندات لديك.
type: docs
weight: 7510
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
| DataLossCategory | `FF` | قد يكون بعض النصوص/الأحرف/الصور أو البيانات الأخرى مفقودة إما من شجرة المستند بعد التحميل، أو من المستند الذي تم إنشاؤه بعد الحفظ. |
| DataLoss | `1` | فقدان البيانات العامة، لا يوجد رمز محدد. |
| MajorFormattingLossCategory | `FF00` | قد يبدو المستند الناتج أو موقع معين فيه مختلفًا بشكل كبير مقارنة بالمستند الأصلي. |
| MajorFormattingLoss | `100` | فقدان تنسيق رئيسي عام، لا يوجد رمز محدد. |
| MinorFormattingLossCategory | `FF0000` | قد يبدو المستند الناتج أو موقع معين فيه مختلفًا بعض الشيء مقارنةً بـ بالمستند الأصلي. |
| MinorFormattingLoss | `10000` | فقدان تنسيق طفيف عام، لا يوجد رمز محدد. |
| FontSubstitution | `20000` | تم استبدال الخط . |
| FontEmbedding | `40000` | فقدان معلومات الخط المضمنة أثناء حفظ المستند. |
| UnexpectedContentCategory | `F000000` | لم يتم التعرف على بعض المحتوى في المستند المصدر (أي أنه غير مدعوم)، وقد يؤدي هذا أو لا يؤدي إلى حدوث مشكلات أو فقدان البيانات/التنسيق. |
| UnexpectedContent | `1000000` | محتوى عام غير متوقع، لا يوجد رمز محدد. |
| Hint | `10000000` | ينصح بوجود مشكلة محتملة أو يقترح تحسينًا. |

## أمثلة

يوضح كيفية تعيين الخاصية للعثور على أقرب تطابق لخط مفقود من مصادر الخطوط المتوفرة.

```csharp
public void EnableFontSubstitution()
{
    // افتح مستندًا يحتوي على نص منسق بخط غير موجود في أي من مصادر الخطوط لدينا.
    Document doc = new Document(MyDir + "Missing font.docx");

    // تعيين معاودة الاتصال للتعامل مع تحذيرات استبدال الخط.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // تعيين اسم الخط الافتراضي وتمكين استبدال الخط.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // ينبغي استخدام مقاييس الخط الأصلية بعد استبدال الخط.
    doc.LayoutOptions.KeepOriginalFontMetrics = true;

    // سوف نحصل على تحذير استبدال الخط إذا قمنا بحفظ مستند بخط مفقود.
    doc.FontSettings = fontSettings;
    doc.Save(ArtifactsDir + "FontSettings.EnableFontSubstitution.pdf");

    using (IEnumerator<WarningInfo> warnings = substitutionWarningHandler.FontWarnings.GetEnumerator())
        while (warnings.MoveNext())
            Console.WriteLine(warnings.Current.Description);

    //يمكننا أيضًا التحقق من التحذيرات الموجودة في المجموعة ومسحها.
    Assert.AreEqual(WarningSource.Layout, substitutionWarningHandler.FontWarnings[0].Source);
    Assert.AreEqual(
        "Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
        substitutionWarningHandler.FontWarnings[0].Description);

    substitutionWarningHandler.FontWarnings.Clear();

    Assert.AreEqual(0, substitutionWarningHandler.FontWarnings.Count);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// يتم استدعاؤها في كل مرة يحدث فيها تحذير أثناء التحميل/الحفظ.
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
