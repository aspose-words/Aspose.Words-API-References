---
title: ImageData.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words لـ .NET
description: ImageData Borders ملكية. الحصول على مجموعة حدود الصورة. الحدود لها تأثير فقط على الصور المضمنة في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing/imagedata/borders/
---
## ImageData.Borders property

الحصول على مجموعة حدود الصورة. الحدود لها تأثير فقط على الصور المضمنة.

```csharp
public BorderCollection Borders { get; }
```

## أمثلة

يوضح كيفية تحرير بيانات صورة الشكل.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape sourceShape = (Shape)imgSourceDoc.GetChildNodes(NodeType.Shape, true)[0];

Document dstDoc = new Document();

// قم باستيراد شكل من المستند المصدر وإلحاقه بالفقرة الأولى.
Shape importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

// الشكل المستورد يحتوي على صورة. يمكننا الوصول إلى خصائص الصورة والبيانات الأولية عبر كائن ImageData.
ImageData imageData = importedShape.ImageData;
imageData.Title = "Imported Image";

Assert.True(imageData.HasImage);

// إذا كانت الصورة ليس لها حدود، فسيحدد كائن ImageData الخاص بها لون الحدود على أنه فارغ.
Assert.AreEqual(4, imageData.Borders.Count);
Assert.AreEqual(Color.Empty, imageData.Borders[0].Color);

// لا ترتبط هذه الصورة بشكل أو ملف صورة آخر في نظام الملفات المحلي.
Assert.False(imageData.IsLink);
Assert.False(imageData.IsLinkOnly);

// تحدد خصائص "السطوع" و"التباين" سطوع الصورة وتباينها
// على مقياس من 0 إلى 1، والقيمة الافتراضية هي 0.5.
imageData.Brightness = 0.8;
imageData.Contrast = 1.0;

// أدت قيم السطوع والتباين المذكورة أعلاه إلى إنشاء صورة بها الكثير من اللون الأبيض.
// يمكننا تحديد لون باستخدام خاصية ChromaKey لاستبداله بالشفافية، مثل الأبيض.
imageData.ChromaKey = Color.White;

// قم باستيراد الشكل المصدر مرة أخرى واضبط الصورة على أحادية اللون.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.GrayScale = true;

// قم باستيراد الشكل المصدر مرة أخرى لإنشاء صورة ثالثة وتعيينها على BiLevel.
// BiLevel يضبط كل بكسل على اللون الأسود أو الأبيض، أيهما أقرب إلى اللون الأصلي.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.BiLevel = true;

// يتم تحديد الاقتصاص على مقياس من 0 إلى 1. اقتصاص الجانب بنسبة 0.3
// سيتم اقتصاص 30% من الصورة من الجانب الذي تم اقتصاصه.
importedShape.ImageData.CropBottom = 0.3;
importedShape.ImageData.CropLeft = 0.3;
importedShape.ImageData.CropTop = 0.3;
importedShape.ImageData.CropRight = 0.3;

dstDoc.Save(ArtifactsDir + "Drawing.ImageData.docx");
```

### أنظر أيضا

* class [BorderCollection](../../../aspose.words/bordercollection/)
* class [ImageData](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
