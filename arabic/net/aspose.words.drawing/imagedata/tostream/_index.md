---
title: ImageData.ToStream
linktitle: ToStream
articleTitle: ToStream
second_title: Aspose.Words لـ .NET
description: ImageData ToStream طريقة. إنشاء وإرجاع دفق يحتوي على بايتات الصورة في C#.
type: docs
weight: 230
url: /ar/net/aspose.words.drawing/imagedata/tostream/
---
## ImageData.ToStream method

إنشاء وإرجاع دفق يحتوي على بايتات الصورة.

```csharp
public Stream ToStream()
```

## ملاحظات

إذا تم تخزين بايتات الصورة في الشكل، فسيتم إنشاء وإرجاع ملفMemoryStream هدف.

إذا كانت الصورة مرتبطة ومخزنة في ملف، فافتح الملف وإرجاع ملفFileStream هدف.

إذا كانت الصورة مرتبطة ومخزنة في عنوان URL خارجي، فسيتم تنزيل الملف وإرجاع ملفMemoryStream هدف.

هل تقع على عاتق المتصل مسؤولية التخلص من كائن الدفق.

## أمثلة

يوضح كيفية إنشاء ملف صورة من بيانات الصورة الأولية للشكل.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape imgShape = (Shape) imgSourceDoc.GetChild(NodeType.Shape, 0, true);

Assert.True(imgShape.HasImage);

// ToByteArray () يُرجع المصفوفة المخزنة في خاصية ImageBytes.
Assert.AreEqual(imgShape.ImageData.ImageBytes, imgShape.ImageData.ToByteArray());

// احفظ بيانات صورة الشكل في ملف صورة في نظام الملفات المحلي.
using (Stream imgStream = imgShape.ImageData.ToStream())
{
    using (FileStream outStream = new FileStream(ArtifactsDir + "Drawing.GetDataFromImage.png",
        FileMode.Create, FileAccess.ReadWrite))
    {
        imgStream.CopyTo(outStream);
    }
}
```

### أنظر أيضا

* class [ImageData](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
