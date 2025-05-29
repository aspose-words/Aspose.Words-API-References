---
title: MetafileRenderingOptions.EmulateRasterOperations
linktitle: EmulateRasterOperations
articleTitle: EmulateRasterOperations
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية MetafileRenderingOptions EmulateRasterOperations للتحكم في محاكاة عملية الراستر، مما يعزز قدرات العرض لديك بشكل فعال.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/
---
## MetafileRenderingOptions.EmulateRasterOperations property

يحصل على قيمة أو يعينها لتحديد ما إذا كان ينبغي محاكاة عمليات الراستر أم لا.

```csharp
public bool EmulateRasterOperations { get; set; }
```

## ملاحظات

يمكن استخدام عمليات نقطية محددة في ملفات التعريف. لا يمكن عرضها مباشرةً على رسومات متجهية. تتطلب محاكاة عمليات النقطية تحويلًا جزئيًا للرسومات المتجهة الناتجة، مما قد يؤثر على أداء عرض ملفات التعريف .

عندما يتم تعيين هذه القيمة على`حقيقي`يحاكي Aspose.Words عمليات الراستر. قد يكون الناتج مُحوّلاً جزئيًا إلى راستر، وقد يكون الأداء أبطأ.

عندما يتم تعيين هذه القيمة على`خطأ شنيع`لا يُحاكي Aspose.Words عمليات الراستر. عند مواجهة Aspose.Words عملية راستر في ملف ميتا، فإنه يلجأ إلى تحويل الملف الميتا إلى خريطة نقطية باستخدام نظام التشغيل .

يتم استخدام هذا الخيار فقط عندما يتم عرض الملف التعريفي كرسومات متجهة.

القيمة الافتراضية هي`حقيقي`.

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

* class [MetafileRenderingOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
