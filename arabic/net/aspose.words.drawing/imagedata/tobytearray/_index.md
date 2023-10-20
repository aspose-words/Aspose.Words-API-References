---
title: ImageData.ToByteArray
linktitle: ToByteArray
articleTitle: ToByteArray
second_title: Aspose.Words لـ .NET
description: ImageData ToByteArray طريقة. إرجاع بايتات الصورة لأي صورة بغض النظر عما إذا كانت الصورة مخزنة أو مرتبطة في C#.
type: docs
weight: 210
url: /ar/net/aspose.words.drawing/imagedata/tobytearray/
---
## ImageData.ToByteArray method

إرجاع بايتات الصورة لأي صورة بغض النظر عما إذا كانت الصورة مخزنة أو مرتبطة.

```csharp
public byte[] ToByteArray()
```

## ملاحظات

إذا كانت الصورة مرتبطة، فسيتم تنزيل الصورة في كل مرة يتم استدعاؤها.

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
