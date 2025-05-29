---
title: ImageData.ToStream
linktitle: ToStream
articleTitle: ToStream
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة ImageData ToStream—تحويل الصور إلى تدفقات بايت بكفاءة للتعامل بسلاسة مع البيانات وتحسين أداء التطبيق.
type: docs
weight: 240
url: /ar/net/aspose.words.drawing/imagedata/tostream/
---
## ImageData.ToStream method

ينشئ ويعيد مجرى يحتوي على بايتات الصورة.

```csharp
public Stream ToStream()
```

## ملاحظات

إذا تم تخزين بايتات الصورة في الشكل، يتم إنشاء وإرجاعMemoryStream هدف.

إذا تم ربط الصورة وتخزينها في ملف، فسيتم فتح الملف وإرجاعFileStream هدف.

إذا تم ربط الصورة وتخزينها في عنوان URL خارجي، فسيتم تنزيل الملف وإرجاعهMemoryStream هدف.

هل تقع على عاتق المتصل مسؤولية التخلص من كائن التدفق؟

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
