---
title: MetafileRenderingOptions Class
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words لـ .NET
description: اكتشف خيارات Aspose.Words.Saving.MetafileRendering لتحسين التحكم في عرض الملفات التعريفية وتخصيصها في مستنداتك. حسّن سير عملك اليوم!
type: docs
weight: 6080
url: /ar/net/aspose.words.saving/metafilerenderingoptions/
---
## MetafileRenderingOptions class

يسمح بتحديد خيارات عرض الملف التعريفي الإضافية.

لمعرفة المزيد، قم بزيارة[التعامل مع ملفات التعريف في Windows](https://docs.aspose.com/words/net/handling-windows-metafiles/) مقالة توثيقية.

```csharp
public class MetafileRenderingOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [MetafileRenderingOptions](metafilerenderingoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [EmfPlusDualRenderingMode](../../aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض ملفات التعريف EMF+ Dual أو يعينها. |
| [EmulateRasterOperations](../../aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان ينبغي محاكاة عمليات الراستر أم لا. |
| [EmulateRenderingToSizeOnPage](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان عرض الملف التعريفي يحاكي عرض الملف التعريفي وفقًا للحجم على page أو عرض الملف التعريفي بحجمه الافتراضي. |
| [EmulateRenderingToSizeOnPageResolution](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/) { get; set; } | يحصل على الدقة بالبكسل لكل بوصة أو يضبطها لمحاكاة عرض الملف التعريفي إلى الحجم الموجود في الصفحة. |
| [RenderingMode](../../aspose.words.saving/metafilerenderingoptions/renderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض صور الملف التعريفي أو يعينها. |
| [UseEmfEmbeddedToWmf](../../aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/) { get; set; } | يحصل على قيمة أو يعينها لتحديد كيفية عرض ملفات تعريف WMF التي تحتوي على ملفات تعريف EMF مضمنة. |
| [UseGdiRasterOperationsEmulation](../../aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم استخدام GDI+ لمحاكاة عمليات الراستر أم لا. |

## أمثلة

يُظهر العرض إضافة بديل لعرض الخريطة النقطية وتغيير نوع التحذيرات حول سجلات الملفات التعريفية غير المدعومة.

```csharp
public void HandleBinaryRasterWarnings()
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // اضبط خاصية "EmulateRasterOperations" على "false" للعودة إلى الخريطة النقطية عندما
    // يواجه ملفًا تعريفيًا، والذي سيتطلب عمليات نقطية لعرضه في ملف PDF الناتج.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // قم بتعيين خاصية "RenderingMode" إلى "VectorWithFallback" لمحاولة عرض كل ملف تعريفي باستخدام الرسومات المتجهة.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
    // لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF وتطبيق التكوين
    // في كائن MetafileRenderingOptions الخاص بنا لعملية الحفظ.
    PdfSaveOptions saveOptions = new PdfSaveOptions();
    saveOptions.MetafileRenderingOptions = metafileRenderingOptions;

    HandleDocumentWarnings callback = new HandleDocumentWarnings();
    doc.WarningCallback = callback;

    doc.Save(ArtifactsDir + "PdfSaveOptions.HandleBinaryRasterWarnings.pdf", saveOptions);

    Assert.AreEqual(1, callback.Warnings.Count);
    Assert.AreEqual("'R2_XORPEN' binary raster operation is not supported.",
        callback.Warnings[0].Description);
}

/// <summary>
/// يطبع ويجمع تحذيرات فقدان التنسيق التي تحدث عند حفظ المستند.
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

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
