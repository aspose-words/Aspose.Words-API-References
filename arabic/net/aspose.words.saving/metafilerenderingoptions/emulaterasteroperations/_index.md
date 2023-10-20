---
title: MetafileRenderingOptions.EmulateRasterOperations
linktitle: EmulateRasterOperations
articleTitle: EmulateRasterOperations
second_title: Aspose.Words لـ .NET
description: MetafileRenderingOptions EmulateRasterOperations ملكية. الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب محاكاة العمليات النقطية أم لا في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/
---
## MetafileRenderingOptions.EmulateRasterOperations property

الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب محاكاة العمليات النقطية أم لا.

```csharp
public bool EmulateRasterOperations { get; set; }
```

## ملاحظات

يمكن استخدام عمليات نقطية محددة في ملفات التعريف. ولا يمكن عرضها مباشرة إلى الرسومات المتجهة. تتطلب محاكاة العمليات النقطية تنقيطًا جزئيًا للرسومات المتجهة الناتجة مما قد يؤثر على أداء عرض ملف التعريف .

عندما يتم ضبط هذه القيمة على`حقيقي`، Aspose.Words يحاكي العمليات النقطية. ربما يكون الإخراج الناتج نقطيًا جزئيًا وقد يكون الأداء أبطأ.

عندما يتم ضبط هذه القيمة على`خطأ شنيع`، Aspose.Words لا يحاكي العمليات النقطية. عندما يواجه Aspose.Words عملية نقطية في ملف تعريف، فإنه يتراجع إلى عرض ملف التعريف في صورة نقطية باستخدام نظام التشغيل .

يتم استخدام هذا الخيار فقط عندما يتم عرض ملف التعريف كرسومات متجهة.

القيمة الافتراضية هي`حقيقي`.

## أمثلة

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

* class [MetafileRenderingOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
