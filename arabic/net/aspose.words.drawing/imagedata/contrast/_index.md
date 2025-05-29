---
title: ImageData.Contrast
linktitle: Contrast
articleTitle: Contrast
second_title: Aspose.Words لـ .NET
description: اضبط تباين الصورة بسهولة باستخدام خاصية ImageData Contrast. اضبط القيم من 0.0 (منخفض) إلى 1.0 (عالي) للحصول على أفضل وضوح وجودة للصورة.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing/imagedata/contrast/
---
## ImageData.Contrast property

يحصل على تباين الصورة المحددة أو يضبطه. يجب أن تكون قيمة لهذه الخاصية رقمًا يتراوح بين 0.0 (أقل تباين) و1.0 (أعلى تباين).

```csharp
public double Contrast { get; set; }
```

## ملاحظات

القيمة الافتراضية هي 0.5.

## أمثلة

يوضح كيفية تحرير بيانات صورة الشكل.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape sourceShape = (Shape)imgSourceDoc.GetChildNodes(NodeType.Shape, true)[0];

Document dstDoc = new Document();

// استيراد شكل من المستند المصدر وإضافته إلى الفقرة الأولى.
Shape importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

// يحتوي الشكل المستورد على صورة. يمكننا الوصول إلى خصائص الصورة وبياناتها الخام عبر كائن ImageData.
ImageData imageData = importedShape.ImageData;
imageData.Title = "Imported Image";

Assert.True(imageData.HasImage);

// إذا لم يكن للصورة حدود، فسوف يحدد كائن ImageData لون الحدود على أنه فارغ.
Assert.AreEqual(4, imageData.Borders.Count);
Assert.AreEqual(Color.Empty, imageData.Borders[0].Color);

// لا ترتبط هذه الصورة بملف شكل أو صورة آخر في نظام الملفات المحلي.
Assert.False(imageData.IsLink);
Assert.False(imageData.IsLinkOnly);

// تحدد خصائص "السطوع" و"التباين" سطوع الصورة وتباينها
// على مقياس من 0 إلى 1، مع القيمة الافتراضية عند 0.5.
imageData.Brightness = 0.8;
imageData.Contrast = 1.0;

// لقد أدت قيم السطوع والتباين المذكورة أعلاه إلى إنشاء صورة تحتوي على قدر كبير من اللون الأبيض.
// يمكننا تحديد لون باستخدام خاصية ChromaKey لاستبداله بالشفافية، مثل اللون الأبيض.
imageData.ChromaKey = Color.White;

// قم باستيراد الشكل المصدر مرة أخرى واضبط الصورة على أحادية اللون.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.GrayScale = true;

// قم باستيراد الشكل المصدر مرة أخرى لإنشاء صورة ثالثة وتعيينها على BiLevel.
// يقوم BiLevel بتعيين كل بكسل إلى اللون الأسود أو الأبيض، أيهما أقرب إلى اللون الأصلي.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.BiLevel = true;

// يُحدَّد القص على مقياس من ٠ إلى ١. قص جانب بمقدار ٠.٣
// سيتم اقتصاص 30% من الصورة عند الجانب المقصوص.
importedShape.ImageData.CropBottom = 0.3;
importedShape.ImageData.CropLeft = 0.3;
importedShape.ImageData.CropTop = 0.3;
importedShape.ImageData.CropRight = 0.3;

dstDoc.Save(ArtifactsDir + "Drawing.ImageData.docx");
```

### أنظر أيضا

* class [ImageData](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
