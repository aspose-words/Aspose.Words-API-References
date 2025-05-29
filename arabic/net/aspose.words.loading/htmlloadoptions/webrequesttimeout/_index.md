---
title: HtmlLoadOptions.WebRequestTimeout
linktitle: WebRequestTimeout
articleTitle: WebRequestTimeout
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية WebRequestTimeout في HtmlLoadOptions، التي تتيح لك تخصيص إعدادات مهلة الانتظار لتحقيق أداء ويب مثالي. افتراضيًا، ١٠٠ ثانية.
type: docs
weight: 80
url: /ar/net/aspose.words.loading/htmlloadoptions/webrequesttimeout/
---
## HtmlLoadOptions.WebRequestTimeout property

عدد الملي ثانية التي يجب انتظارها قبل انتهاء مهلة طلب الويب. القيمة الافتراضية هي ١٠٠٠٠٠ ميلي ثانية (١٠٠ ثانية).

```csharp
public int WebRequestTimeout { get; set; }
```

## ملاحظات

عدد المللي ثانية التي ينتظرها Aspose.Words للحصول على استجابة، عند تحميل الموارد الخارجية (الصور، وأوراق style ) المرتبطة في مستندات HTML وMHTML.

## أمثلة

يوضح كيفية تعيين حد زمني لطلبات الويب عند تحميل مستند يحتوي على موارد خارجية مرتبطة بعناوين URL.

```csharp
public void WebRequestTimeout()
{
    // قم بإنشاء كائن HtmlLoadOptions جديد وتحقق من حد المهلة لطلب الويب.
    HtmlLoadOptions options = new HtmlLoadOptions();

    // عند تحميل مستند HTML يحتوي على موارد مرتبطة خارجيًا بواسطة عنوان URL على الويب،
    // سيقوم Aspose.Words بإلغاء طلبات الويب التي تفشل في جلب الموارد خلال هذا الحد الزمني، بالمللي ثانية.
    Assert.AreEqual(100000, options.WebRequestTimeout);

    // قم بتعيين WarningCallback الذي سيسجل جميع التحذيرات التي تحدث أثناء التحميل.
    ListDocumentWarnings warningCallback = new ListDocumentWarnings();
    options.WarningCallback = warningCallback;

    // قم بتحميل مثل هذا المستند وتأكد من إنشاء شكل يحتوي على بيانات الصورة.
    // ستتطلب هذه الصورة المرتبطة طلب ويب للتحميل، والذي يجب أن يكتمل خلال الحد الزمني لدينا.
    string html = $@"
        <html>
            <img src=""{ImageUrl}"" alt=""Aspose logo"" style=""width:400px;height:400px;"">
        </html>
    ";

    // قم بتعيين حد زمني غير معقول وحاول تحميل المستند مرة أخرى.
    options.WebRequestTimeout = 0;
    Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), options);
    Assert.AreEqual(2, warningCallback.Warnings().Count);

    // سيظل طلب الويب الذي يفشل في الحصول على صورة ضمن المهلة الزمنية ينتج صورة.
    // ومع ذلك، ستكون الصورة عبارة عن علامة "x" الحمراء التي تشير عادةً إلى الصور المفقودة.
    Shape imageShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
    Assert.AreEqual(924, imageShape.ImageData.ImageBytes.Length);

    // يمكننا أيضًا تكوين معاودة اتصال مخصصة لالتقاط أي تحذيرات من طلبات الويب التي انتهت صلاحيتها.
    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[0].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[0].WarningType);
    Assert.AreEqual($"Couldn't load a resource from \'{ImageUrl}\'.", warningCallback.Warnings()[0].Description);

    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[1].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[1].WarningType);
    Assert.AreEqual("Image has been replaced with a placeholder.", warningCallback.Warnings()[1].Description);

    doc.Save(ArtifactsDir + "HtmlLoadOptions.WebRequestTimeout.docx");
}

/// <summary>
/// يخزن جميع التحذيرات التي تحدث أثناء عملية تحميل المستند في قائمة.
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
