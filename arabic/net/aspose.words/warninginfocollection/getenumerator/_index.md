---
title: WarningInfoCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words لـ .NET
description: WarningInfoCollection GetEnumerator طريقة. إرجاع كائن العداد الذي يمكن استخدامه للتكرار على كافة العناصر الموجودة في المجموعة في C#.
type: docs
weight: 50
url: /ar/net/aspose.words/warninginfocollection/getenumerator/
---
## WarningInfoCollection.GetEnumerator method

إرجاع كائن العداد الذي يمكن استخدامه للتكرار على كافة العناصر الموجودة في المجموعة.

```csharp
public IEnumerator<WarningInfo> GetEnumerator()
```

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

* class [WarningInfo](../../warninginfo/)
* class [WarningInfoCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
