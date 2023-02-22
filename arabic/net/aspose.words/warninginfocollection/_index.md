---
title: Class WarningInfoCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.WarningInfoCollection فصل. يمثل مجموعة مكتوبة منWarningInfo الكائنات .
type: docs
weight: 6330
url: /ar/net/aspose.words/warninginfocollection/
---
## WarningInfoCollection class

يمثل مجموعة مكتوبة من[`WarningInfo`](../warninginfo/) الكائنات .

```csharp
public class WarningInfoCollection : IEnumerable<WarningInfo>, IWarningCallback
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [WarningInfoCollection](warninginfocollection/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/warninginfocollection/count/) { get; } | الحصول على عدد العناصر الموجودة في المجموعة. |
| [Item](../../aspose.words/warninginfocollection/item/) { get; } | الحصول على عنصر بالفهرس المحدد . |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clear](../../aspose.words/warninginfocollection/clear/)() | يزيل كل العناصر من المجموعة. |
| [GetEnumerator](../../aspose.words/warninginfocollection/getenumerator/)() | إرجاع كائن العداد الذي يمكن استخدامه للتكرار على كافة العناصر في المجموعة. |
| [Warning](../../aspose.words/warninginfocollection/warning/)(WarningInfo) | تنفذ ملف[`IWarningCallback`](../iwarningcallback/) واجهه المستخدم. يضيف تحذيرًا إلى هذه المجموعة . |

### ملاحظات

يمكنك استخدام كائن المجموعة هذا كأبسط شكل من أشكال[`IWarningCallback`](../iwarningcallback/)التطبيق لجمع جميع التحذيرات التي تولدها Aspose.Words أثناء عملية التحميل أو الحفظ. قم بإنشاء مثيل لهذه الفئة وقم بتعيينه إلى ملف[`WarningCallback`](../../aspose.words.loading/loadoptions/warningcallback/) أو[`WarningCallback`](../documentbase/warningcallback/) منشأه.

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

* class [WarningInfo](../warninginfo/)
* interface [IWarningCallback](../iwarningcallback/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


