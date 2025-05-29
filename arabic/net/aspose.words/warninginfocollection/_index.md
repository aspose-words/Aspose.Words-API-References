---
title: WarningInfoCollection Class
linktitle: WarningInfoCollection
articleTitle: WarningInfoCollection
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.WarningInfoCollection، وهي فئة قوية لإدارة كائنات WarningInfo، وتحسين معالجة المستندات والتعامل مع الأخطاء.
type: docs
weight: 7490
url: /ar/net/aspose.words/warninginfocollection/
---
## WarningInfoCollection class

يمثل مجموعة مكتوبة من[`WarningInfo`](../warninginfo/) الأشياء.

لمعرفة المزيد، قم بزيارة[البرمجة باستخدام المستندات](https://docs.aspose.com/words/net/programming-with-documents/) مقالة توثيقية.

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
| [Count](../../aspose.words/warninginfocollection/count/) { get; } | يحصل على عدد العناصر الموجودة في المجموعة. |
| [Item](../../aspose.words/warninginfocollection/item/) { get; } | يحصل على عنصر في الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clear](../../aspose.words/warninginfocollection/clear/)() | يزيل جميع العناصر من المجموعة. |
| [GetEnumerator](../../aspose.words/warninginfocollection/getenumerator/)() | يعيد كائن عداد يمكن استخدامه للتكرار على جميع العناصر في المجموعة. |
| [Warning](../../aspose.words/warninginfocollection/warning/)(*[WarningInfo](../warninginfo/)*) | ينفذ[`IWarningCallback`](../iwarningcallback/) الواجهة. إضافة تحذير إلى هذه المجموعة. |

## ملاحظات

يمكنك استخدام كائن المجموعة هذا باعتباره أبسط شكل لـ[`IWarningCallback`](../iwarningcallback/) تطبيق لجمع جميع التحذيرات التي يُنشئها Aspose.Words أثناء عملية التحميل أو الحفظ. أنشئ مثيلًا لهذه الفئة وعيّنه إلى [`WarningCallback`](../../aspose.words.loading/loadoptions/warningcallback/) أو[`WarningCallback`](../documentbase/warningcallback/) ملكية.

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

* class [WarningInfo](../warninginfo/)
* interface [IWarningCallback](../iwarningcallback/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
