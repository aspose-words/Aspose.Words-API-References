---
title: LoadOptions.BaseUri
linktitle: BaseUri
articleTitle: BaseUri
second_title: Aspose.Words لـ .NET
description: LoadOptions BaseUri ملكية. الحصول على أو تعيين السلسلة التي سيتم استخدامها لتحليل معرفات URI النسبية الموجودة في المستند إلى معرفات URI مطلقة عند الحاجة. يمكن أن يكونباطل أو سلسلة فارغة. الافتراضي هوباطل  في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.loading/loadoptions/baseuri/
---
## LoadOptions.BaseUri property

الحصول على أو تعيين السلسلة التي سيتم استخدامها لتحليل معرفات URI النسبية الموجودة في المستند إلى معرفات URI مطلقة عند الحاجة. يمكن أن يكون`باطل` أو سلسلة فارغة. الافتراضي هو`باطل` .

```csharp
public string BaseUri { get; set; }
```

## ملاحظات

تُستخدم هذه الخاصية لتحويل عناوين URI النسبية إلى مطلقة في الحالات التالية:

1. عند تحميل مستند HTML من دفق ويحتوي المستند على صور تحتوي على معرفات URI نسبية ولا يحتوي على معرف URI أساسي محدد في عنصر BASE HTML.
2. عند حفظ مستند إلى PDF وتنسيقات أخرى، يمكنك استرداد الصور المرتبطة باستخدام URIs النسبية بحيث يمكن حفظ الصور في مستند الإخراج.

## أمثلة

يوضح كيفية فتح مستند HTML يحتوي على صور من دفق باستخدام عنوان URI أساسي.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // قم بتمرير URI للمجلد الأساسي أثناء تحميله
    // بحيث يمكن العثور على أي صور ذات عناوين URI نسبية في مستند HTML.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // تحقق من أن الشكل الأول للمستند يحتوي على صورة صالحة.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### أنظر أيضا

* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
