---
title: DocumentBase.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية WarningCallback في DocumentBase، وهي خاصية حيوية لضمان سلامة البيانات أثناء معالجة المستندات من خلال اكتشاف مشكلات التنسيق المحتملة.
type: docs
weight: 100
url: /ar/net/aspose.words/documentbase/warningcallback/
---
## DocumentBase.WarningCallback property

يتم استدعاؤها أثناء إجراءات معالجة المستندات المختلفة عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## ملاحظات

قد يُصدر مستند تحذيرات في أي مرحلة من مراحل وجوده، لذا من المهم إعداد استدعاء تحذيري في أسرع وقت ممكن لتجنب فقدان التحذيرات. على سبيل المثال، خصائص مثل[`PageCount`](../../document/pagecount/) يقوم في الواقع ببناء تخطيط المستند الذي سيتم استخدامه لاحقًا للرسم، وقد يتم فقدان تحذيرات التخطيط إذا تم تحديد استدعاء تحذير فقط لمكالمات الرسم لاحقًا.

## أمثلة

يوضح كيفية استخدام واجهة IWarningCallback لمراقبة تحذيرات استبدال الخط.

```csharp
public void SubstitutionWarning()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Times New Roman";
    builder.Writeln("Hello world!");

    FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
    doc.WarningCallback = callback;

    // قم بتخزين المجموعة الحالية من مصادر الخطوط، والتي ستكون مصدر الخط الافتراضي لكل مستند
    // حيث لا نحدد مصدر خط مختلف.
    FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

    // لأغراض الاختبار، سنقوم بتعيين Aspose.Words للبحث عن الخطوط فقط في مجلد غير موجود.
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // عند عرض المستند، لن يكون هناك مكان للعثور على الخط "Times New Roman".
    // سيؤدي هذا إلى ظهور تحذير استبدال الخط، والذي ستكتشفه معاودة الاتصال الخاصة بنا.
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].WarningType == WarningType.FontSubstitution);
    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
}

private class FontSubstitutionWarningCollector : IWarningCallback
{
    /// <summary>
    /// يتم استدعاؤها في كل مرة يحدث فيها تحذير أثناء التحميل/الحفظ.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontSubstitutionWarnings.Warning(info);
    }

    public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

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

* interface [IWarningCallback](../../iwarningcallback/)
* class [DocumentBase](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
