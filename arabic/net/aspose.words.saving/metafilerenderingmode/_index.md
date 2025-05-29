---
title: MetafileRenderingMode Enum
linktitle: MetafileRenderingMode
articleTitle: MetafileRenderingMode
second_title: Aspose.Words لـ .NET
description: اكتشف كيف يعمل Aspose.Words.Saving.MetafileRenderingMode على تعزيز عرض ملفات التعريف WMF وEMF للحصول على جودة وأداء مثاليين للمستندات.
type: docs
weight: 6070
url: /ar/net/aspose.words.saving/metafilerenderingmode/
---
## MetafileRenderingMode enumeration

يحدد كيفية قيام Aspose.Words بعرض ملفات التعريف WMF وEMF.

```csharp
public enum MetafileRenderingMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| VectorWithFallback | `0` | يحاول Aspose.Words عرض ملف تعريفي كرسومات متجهة. إذا لم يتمكن Aspose.Words من عرض بعض سجلات ملف التعريف بشكل صحيح إلى رسومات متجهة، فسيعرض هذا الملف التعريفي على شكل خريطة نقطية. |
| Vector | `1` | يقوم Aspose.Words بعرض ملف تعريفي كرسومات متجهة. |
| Bitmap | `2` | يستدعي Aspose.Words GDI+ لعرض ملف تعريفي على خريطة بتات ثم يحفظ خريطة البتات في مستند الإخراج. |

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
