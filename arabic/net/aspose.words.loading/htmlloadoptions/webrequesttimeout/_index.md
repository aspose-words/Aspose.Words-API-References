---
title: HtmlLoadOptions.WebRequestTimeout
linktitle: WebRequestTimeout
articleTitle: WebRequestTimeout
second_title: Aspose.Words لـ .NET
description: HtmlLoadOptions WebRequestTimeout ملكية. عدد المللي ثانية التي يجب انتظارها قبل انتهاء مهلة طلب الويب. القيمة الافتراضية هي 100000 مللي ثانية 100 ثانية في C#.
type: docs
weight: 70
url: /ar/net/aspose.words.loading/htmlloadoptions/webrequesttimeout/
---
## HtmlLoadOptions.WebRequestTimeout property

عدد المللي ثانية التي يجب انتظارها قبل انتهاء مهلة طلب الويب. القيمة الافتراضية هي 100000 مللي ثانية (100 ثانية).

```csharp
public int WebRequestTimeout { get; set; }
```

## ملاحظات

عدد المللي ثانية التي ينتظرها Aspose.Words للاستجابة، عند تحميل الموارد الخارجية (الصور، style Sheets) المرتبطة في مستندات HTML وMHTML.

## أمثلة

يوضح كيفية تعيين حد زمني لطلبات الويب عند تحميل مستند بموارد خارجية مرتبطة بعناوين URL.

```csharp
public void WebRequestTimeout()
{
    // قم بإنشاء كائن HtmlLoadOptions جديد وتحقق من حد المهلة الخاص به لطلب الويب.
    HtmlLoadOptions options = new HtmlLoadOptions();

    // عند تحميل مستند Html يحتوي على موارد مرتبطة خارجيًا بعنوان URL لعنوان الويب،
    // Aspose.Words سوف يلغي طلبات الويب التي تفشل في جلب الموارد خلال هذا الحد الزمني، بالمللي ثانية.
    Assert.AreEqual(100000, options.WebRequestTimeout);

    // قم بتعيين WaringCallback الذي سيسجل جميع التحذيرات التي تحدث أثناء التحميل.
    ListDocumentWarnings warningCallback = new ListDocumentWarnings();
    options.WarningCallback = warningCallback;

    // قم بتحميل مثل هذا المستند وتحقق من إنشاء شكل يحتوي على بيانات الصورة.
    // ستتطلب هذه الصورة المرتبطة طلب ويب للتحميل، والذي يجب إكماله خلال المهلة الزمنية المحددة لدينا.
    string html = $@"
        <html>
            <img src=""{ImageUrl}"" alt=""Aspose logo"" style=""width:400px;height:400px;"">
        </html>
    ";

    // قم بتعيين حد مهلة غير معقول وحاول تحميل المستند مرة أخرى.
    options.WebRequestTimeout = 0;
    Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), options);
    Assert.AreEqual(2, warningCallback.Warnings().Count);

    // طلب الويب الذي يفشل في الحصول على صورة خلال المهلة الزمنية سيستمر في إنتاج صورة.
    // ومع ذلك، ستكون الصورة علامة "x" الحمراء التي تشير عادةً إلى الصور المفقودة.
    Shape imageShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
    Assert.AreEqual(924, imageShape.ImageData.ImageBytes.Length);

    // يمكننا أيضًا تكوين رد اتصال مخصص لالتقاط أي تحذيرات من طلبات الويب التي انتهت مهلتها.
    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[0].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[0].WarningType);
    Assert.AreEqual($"Couldn't load a resource from \'{ImageUrl}\'.", warningCallback.Warnings()[0].Description);

    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[1].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[1].WarningType);
    Assert.AreEqual("Image has been replaced with a placeholder.", warningCallback.Warnings()[1].Description);

    doc.Save(ArtifactsDir + "HtmlLoadOptions.WebRequestTimeout.docx");
}

/// <summary>
/// يخزن كافة التحذيرات التي تحدث أثناء عملية تحميل المستند في قائمة.
/// </summary>
private class ListDocumentWarnings : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        mWarnings.Add(info);
    }

    public List<WarningInfo> Warnings() { 
        return mWarnings;
    }

    private readonly List<WarningInfo> mWarnings = new List<WarningInfo>();
}
```

### أنظر أيضا

* class [HtmlLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
