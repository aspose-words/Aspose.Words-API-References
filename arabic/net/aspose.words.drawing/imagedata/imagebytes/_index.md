---
title: ImageData.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words لـ .NET
description: ImageData ImageBytes ملكية. الحصول على أو تعيين البايتات الأولية للصورة المخزنة في الشكل في C#.
type: docs
weight: 120
url: /ar/net/aspose.words.drawing/imagedata/imagebytes/
---
## ImageData.ImageBytes property

الحصول على أو تعيين البايتات الأولية للصورة المخزنة في الشكل.

```csharp
public byte[] ImageBytes { get; set; }
```

## ملاحظات

ضبط القيمة على`باطل` أو ستقوم مجموعة فارغة بإزالة الصورة من الشكل.

عائدات`باطل` إذا لم تكن الصورة مخزنة في المستند (على سبيل المثال، من المحتمل أن تكون الصورة مرتبطة في هذه الحالة).

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
