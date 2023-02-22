---
title: Class WarningInfo
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.WarningInfo فصل. يحتوي على معلومات حول تحذير أصدره Aspose.Words أثناء تحميل المستندات أو حفظها.
type: docs
weight: 6320
url: /ar/net/aspose.words/warninginfo/
---
## WarningInfo class

يحتوي على معلومات حول تحذير أصدره Aspose.Words أثناء تحميل المستندات أو حفظها.

```csharp
public class WarningInfo
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Description](../../aspose.words/warninginfo/description/) { get; } | إرجاع وصف التحذير . |
| [Source](../../aspose.words/warninginfo/source/) { get; } | إرجاع مصدر التحذير . |
| [WarningType](../../aspose.words/warninginfo/warningtype/) { get; } | إرجاع نوع التحذير . |

### ملاحظات

لا تقوم بإنشاء نسخ من هذه الفئة. يتم إنشاء كائنات هذه الفئة وتمريرها بواسطة Aspose.Words إلى[`Warning`](../iwarningcallback/warning/) طريقة.

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


