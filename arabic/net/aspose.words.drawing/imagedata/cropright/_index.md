---
title: ImageData.CropRight
linktitle: CropRight
articleTitle: CropRight
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ImageData CropRight، وتحكم في اقتصاص الصورة من الجانب الأيمن لتحرير الصورة بدقة وتحسين جاذبيتها البصرية.
type: docs
weight: 80
url: /ar/net/aspose.words.drawing/imagedata/cropright/
---
## ImageData.CropRight property

يحدد جزء إزالة الصورة من الجانب الأيمن.

```csharp
public double CropRight { get; set; }
```

## ملاحظات

يمكن أن تتراوح قيمة الاقتصاص بين -1.0 و1.0. القيمة الافتراضية هي 0. لاحظ أن قيمة 1 لن تعرض أي صورة على الإطلاق. القيم السالبة ستؤدي إلى ضغط الصورة للداخل من الحافة المقصوصة (سيتم ملء المساحة الفارغة بين الصورة والحافة المقصوصة بلون تعبئة الشكل ). القيم الموجبة الأقل من 1 ستؤدي إلى تمديد الصورة المتبقية لتتناسب مع الشكل.

القيمة الافتراضية هي 0.

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
