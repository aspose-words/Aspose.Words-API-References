---
title: WarningInfo Class
linktitle: WarningInfo
articleTitle: WarningInfo
second_title: Aspose.Words لـ .NET
description: Aspose.Words.WarningInfo فصل. يحتوي على معلومات حول التحذير الذي أصدره Aspose.Words أثناء تحميل المستند أو حفظه في C#.
type: docs
weight: 6630
url: /ar/net/aspose.words/warninginfo/
---
## WarningInfo class

يحتوي على معلومات حول التحذير الذي أصدره Aspose.Words أثناء تحميل المستند أو حفظه.

لمعرفة المزيد، قم بزيارة[البرمجة بالوثائق](https://docs.aspose.com/words/net/programming-with-documents/) مقالة توثيقية.

```csharp
public class WarningInfo
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Description](../../aspose.words/warninginfo/description/) { get; } | يُرجع وصف التحذير. |
| [Source](../../aspose.words/warninginfo/source/) { get; } | إرجاع مصدر التحذير. |
| [WarningType](../../aspose.words/warninginfo/warningtype/) { get; } | يُرجع نوع التحذير. |

## ملاحظات

لا تقم بإنشاء مثيلات هذه الفئة. يتم إنشاء كائنات هذه الفئة وتمريرها بواسطة Aspose.Words إلى ملف[`Warning`](../iwarningcallback/warning/) طريقة.

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
