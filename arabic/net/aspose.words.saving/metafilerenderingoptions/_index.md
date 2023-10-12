---
title: Class MetafileRenderingOptions
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.MetafileRenderingOptions فصل. يسمح بتحديد خيارات عرض ملف التعريف الإضافية.
type: docs
weight: 5300
url: /ar/net/aspose.words.saving/metafilerenderingoptions/
---
## MetafileRenderingOptions class

يسمح بتحديد خيارات عرض ملف التعريف الإضافية.

لمعرفة المزيد، قم بزيارة[التعامل مع ملفات تعريف ويندوز](https://docs.aspose.com/words/net/handling-windows-metafiles/) مقالة توثيقية.

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
| [EmfPlusDualRenderingMode](../../aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض ملفات تعريف EMF+ Dual. |
| [EmulateRasterOperations](../../aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب محاكاة العمليات النقطية أم لا. |
| [EmulateRenderingToSizeOnPage](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان عرض ملف التعريف يحاكي عرض ملف التعريف وفقًا للحجم الموجود على page أو عرض ملف التعريف بحجمه الافتراضي. |
| [EmulateRenderingToSizeOnPageResolution](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/) { get; set; } | الحصول على الدقة بالبكسل في البوصة أو تعيينها لمحاكاة عرض ملف التعريف حسب الحجم الموجود على الصفحة. |
| [RenderingMode](../../aspose.words.saving/metafilerenderingoptions/renderingmode/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض صور ملف التعريف. |
| [UseEmfEmbeddedToWmf](../../aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض ملفات تعريف WMF مع ملفات تعريف EMF المضمنة. |
| [UseGdiRasterOperationsEmulation](../../aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم استخدام GDI+ لمحاكاة العمليات النقطية أم لا. |

### أمثلة

تمت إضافة بديل لعرض الصور النقطية وتغيير نوع التحذيرات حول سجلات ملفات التعريف غير المدعومة.

```csharp
public void HandleBinaryRasterWarnings()
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // قم بتعيين خاصية "EmulateRasterOperations" على "خطأ" للرجوع إلى الصورة النقطية عندما
    // يواجه ملف تعريف، والذي سيتطلب عمليات نقطية لعرضه في ملف PDF الناتج.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // قم بتعيين خاصية "RenderingMode" على "VectorWithFallback" لمحاولة عرض كل ملف تعريف باستخدام الرسومات المتجهة.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
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
/// يطبع ويجمع التحذيرات المتعلقة بفقدان التنسيق التي تحدث عند حفظ المستند.
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


