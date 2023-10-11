---
title: FixedPageSaveOptions.MetafileRenderingOptions
second_title: Aspose.Words لمراجع .NET API
description: FixedPageSaveOptions ملكية. يسمح بتحديد خيارات عرض ملف التعريف.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/
---
## FixedPageSaveOptions.MetafileRenderingOptions property

يسمح بتحديد خيارات عرض ملف التعريف.

```csharp
public MetafileRenderingOptions MetafileRenderingOptions { get; set; }
```

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

* class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* class [FixedPageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../fixedpagesaveoptions/)
* المجسم [Aspose.Words](../../../)


