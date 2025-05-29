---
title: ShapeBase.IsImage
linktitle: IsImage
articleTitle: IsImage
second_title: Aspose.Words لـ .NET
description: اكتشف ما إذا كان الشكل صورة باستخدام خاصية IsImage في ShapeBase. حدّد أشكال الصور بسهولة لتحسين مرونة التصميم ووظائفه.
type: docs
weight: 300
url: /ar/net/aspose.words.drawing/shapebase/isimage/
---
## ShapeBase.IsImage property

إرجاع`حقيقي` إذا كان هذا الشكل هو شكل صورة.

```csharp
public bool IsImage { get; }
```

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

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
