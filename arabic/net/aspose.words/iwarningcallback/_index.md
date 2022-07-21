---
title: IWarningCallback
second_title: Aspose.Words لمراجع .NET API
description: قم بتنفيذ هذه الواجهة إذا كنت تريد أن يكون لديك أسلوب مخصص خاص بك يسمى التقاط تحذيرات فقدان الدقة التي يمكن أن تحدث أثناء تحميل المستند أو حفظه .
type: docs
weight: 3010
url: /ar/net/aspose.words/iwarningcallback/
---
## IWarningCallback interface

قم بتنفيذ هذه الواجهة إذا كنت تريد أن يكون لديك أسلوب مخصص خاص بك يسمى التقاط تحذيرات فقدان الدقة التي يمكن أن تحدث أثناء تحميل المستند أو حفظه .

```csharp
public interface IWarningCallback
```

## طُرق

| اسم | وصف |
| --- | --- |
| [Warning](../../aspose.words/iwarningcallback/warning)(WarningInfo) | Aspose.Words تستدعي هذه الطريقة عندما تواجه بعض المشاكل أثناء تحميل المستند أو الحفظ الذي قد يؤدي إلى فقدان التنسيق أو دقة البيانات . |

### أمثلة

يوضح كيفية استخدام واجهة IWarningCallback لمراقبة تحذيرات استبدال الخط.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Times New Roman";
    builder.Writeln("Hello world!");

    FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
    doc.WarningCallback = callback;

    // قم بتخزين المجموعة الحالية من مصادر الخطوط ، والتي ستكون مصدر الخط الافتراضي لكل مستند
    // التي لم نحدد مصدر خط مختلف لها.
    FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

    // لأغراض الاختبار ، سنقوم بتعيين Aspose.Words للبحث عن الخطوط فقط في مجلد غير موجود.
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // عند تقديم المستند ، لن يكون هناك مكان للعثور على الخط "Times New Roman".
    // سيؤدي هذا إلى تحذير بشأن استبدال الخط ، والذي سيكتشفه رد الاتصال الخاص بنا.
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
}

private class FontSubstitutionWarningCollector : IWarningCallback
{
    /// <summary>
    /// يتم الاتصال به في كل مرة يظهر فيها تحذير أثناء التحميل / الحفظ.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontSubstitutionWarnings.Warning(info);
    }

    public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

أضافت العروض رجوعًا إلى عرض الصور النقطية وتغيير نوع التحذيرات حول سجلات ملفات التعريف غير المدعومة.

```csharp
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // قم بتعيين خاصية "EmulateRasterOperations" على "false" للرجوع إلى الصورة النقطية عندما
    // يواجه ملف تعريف ، والذي سيتطلب عمليات نقطية لتقديمه في ملف PDF الناتج.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // عيّن خاصية "RenderingMode" على "VectorWithFallback" لمحاولة تقديم كل ملف تعريف باستخدام رسومات متجهة.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
    // لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF وتطبيق التكوين
    // في كائن MetafileRenderingOptions الخاص بنا إلى عملية الحفظ.
    PdfSaveOptions saveOptions = new PdfSaveOptions();
    saveOptions.MetafileRenderingOptions = metafileRenderingOptions;

    HandleDocumentWarnings callback = new HandleDocumentWarnings();
    doc.WarningCallback = callback;

    doc.Save(ArtifactsDir + "PdfSaveOptions.HandleBinaryRasterWarnings.pdf", saveOptions);

    Assert.AreEqual(1, callback.Warnings.Count);
    Assert.AreEqual("'R2_XORPEN' binary raster operation is partly supported.",
        callback.Warnings[0].Description);
}

/// <summary>
/// يطبع ويجمع التحذيرات المتعلقة بضياع التنسيق التي تحدث عند حفظ مستند.
/// </summary>
public class HandleDocumentWarnings : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.MinorFormattingLoss)
        {
            Console.WriteLine("Unsupported operation: " + info.Description);
            Warnings.Warning(info);
        }
    }

    public WarningInfoCollection Warnings = new WarningInfoCollection();
}
```

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

* مساحة الاسم [Aspose.Words](../../aspose.words)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
