---
title: Class FontInfoSubstitutionRule
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fonts.FontInfoSubstitutionRule فصل. قاعدة استبدال معلومات الخط .
type: docs
weight: 2760
url: /ar/net/aspose.words.fonts/fontinfosubstitutionrule/
---
## FontInfoSubstitutionRule class

قاعدة استبدال معلومات الخط .

```csharp
public class FontInfoSubstitutionRule : FontSubstitutionRule
```

## الخصائص

| اسم | وصف |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | يحدد ما إذا كانت القاعدة ممكّنة أم لا. |

### ملاحظات

وفقًا لهذه القاعدة ، تقوم Aspose.Words بتقييم جميع الحقول ذات الصلة في[`FontInfo`](../fontinfo/) (Panose ، Sig ، إلخ) for الخط المفقود والعثور على أقرب تطابق بين مصادر الخطوط المتاحة. إذا[`FontInfo`](../fontinfo/) is not متاحًا للخط المفقود ، فلن يتم فعل أي شيء.

### أمثلة

يوضح كيفية تعيين الخاصية للعثور على أقرب تطابق لخط مفقود من مصادر الخط المتاحة.

```csharp
[Test]
public void EnableFontSubstitution()
{
    // افتح مستندًا يحتوي على نص منسق بخط غير موجود في أي من مصادر الخطوط لدينا.
    Document doc = new Document(MyDir + "Missing font.docx");

    // تعيين رد اتصال للتعامل مع تحذيرات استبدال الخط.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // تعيين اسم الخط الافتراضي وتمكين استبدال الخط.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // سنحصل على تحذير بشأن استبدال الخط إذا حفظنا مستندًا بخط مفقود.
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
    /// يتم الاتصال به في كل مرة يظهر فيها تحذير أثناء التحميل / الحفظ.
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

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)


