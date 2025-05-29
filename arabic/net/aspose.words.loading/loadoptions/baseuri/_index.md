---
title: LoadOptions.BaseUri
linktitle: BaseUri
articleTitle: BaseUri
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية LoadOptions BaseUri لتحويل عناوين URI النسبية إلى عناوين URI مطلقة بسهولة في مستنداتك. حسّن إدارة عناوين URI الخاصة بك اليوم!
type: docs
weight: 20
url: /ar/net/aspose.words.loading/loadoptions/baseuri/
---
## LoadOptions.BaseUri property

يحصل على السلسلة التي سيتم استخدامها لتحويل عناوين URI النسبية الموجودة في المستند إلى عناوين URI مطلقة عند الحاجة إليها أو يعينها. يمكن أن يكون`باطل` أو سلسلة فارغة. الافتراضي هو`باطل` .

```csharp
public string BaseUri { get; set; }
```

## ملاحظات

يتم استخدام هذه الخاصية لتحويل عناوين URI النسبية إلى عناوين مطلقة في الحالات التالية:

1. عند تحميل مستند HTML من مجرى ويحتوي المستند على صور ذات عناوين URI نسبية ولا يحتوي على عنوان URI أساسي محدد في عنصر HTML الأساسي.
2. عند حفظ مستند بتنسيق PDF وتنسيقات أخرى، لاسترداد الصور المرتبطة باستخدام URIs النسبي حتى يمكن حفظ الصور في مستند الإخراج.

## أمثلة

يوضح كيفية فتح مستند HTML يحتوي على صور من مجرى باستخدام عنوان URI أساسي.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // قم بتمرير عنوان URI للمجلد الأساسي أثناء تحميله
    // بحيث يمكن العثور على أي صور تحتوي على عناوين URI نسبية في مستند HTML.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // تأكد من أن الشكل الأول للمستند يحتوي على صورة صالحة.
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
