---
title: ImageData.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ImageData ImageBytes لإدارة بايتات الصور الخام ومعالجتها بسهولة داخل الأشكال الخاصة بك للحصول على محتوى مرئي محسّن.
type: docs
weight: 120
url: /ar/net/aspose.words.drawing/imagedata/imagebytes/
---
## ImageData.ImageBytes property

يحصل على البايتات الخام للصورة المخزنة في الشكل أو يعينها.

```csharp
public byte[] ImageBytes { get; set; }
```

## ملاحظات

تعيين القيمة إلى`باطل` أو سيؤدي استخدام مصفوفة فارغة إلى إزالة الصورة من الشكل.

الإرجاعات`باطل` إذا لم يتم تخزين الصورة في المستند (على سبيل المثال، من المحتمل أن تكون الصورة مرتبطة في هذه الحالة).

## أمثلة

يوضح كيفية إنشاء ملف صورة من بيانات الصورة الخام للشكل.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape imgShape = (Shape) imgSourceDoc.GetChild(NodeType.Shape, 0, true);

Assert.True(imgShape.HasImage);

// تقوم ToByteArray() بإرجاع المصفوفة المخزنة في خاصية ImageBytes.
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
