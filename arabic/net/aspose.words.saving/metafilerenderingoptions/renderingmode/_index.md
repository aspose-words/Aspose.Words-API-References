---
title: MetafileRenderingOptions.RenderingMode
linktitle: RenderingMode
articleTitle: RenderingMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية MetafileRenderingOptions RenderingMode للتحكم في كيفية عرض صور الملف التعريفي، مما يعزز جودة الرسومات والأداء.
type: docs
weight: 60
url: /ar/net/aspose.words.saving/metafilerenderingoptions/renderingmode/
---
## MetafileRenderingOptions.RenderingMode property

يحصل على قيمة تحدد كيفية عرض صور الملف التعريفي أو يعينها.

```csharp
public MetafileRenderingMode RenderingMode { get; set; }
```

## ملاحظات

تعتمد القيمة الافتراضية على تنسيق الحفظ. بالنسبة للصور، تكونBitmap . بالنسبة للتنسيقات الأخرى فهوVectorWithFallback.

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

* enum [MetafileRenderingMode](../../metafilerenderingmode/)
* class [MetafileRenderingOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
