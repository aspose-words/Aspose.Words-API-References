---
title: Fill.PresetTexture
linktitle: PresetTexture
articleTitle: PresetTexture
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية ضبط خاصية PresetTexture بسهولة، وحسّن تصميماتك بخيارات تعبئة مذهلة. أطلق العنان لإبداعك اليوم!
type: docs
weight: 170
url: /ar/net/aspose.words.drawing/fill/presettexture/
---
## Fill.PresetTexture property

يحصل على[`PresetTexture`](../../presettexture/) للتعبئة.

```csharp
public PresetTexture PresetTexture { get; }
```

## أمثلة

يوضح كيفية ملء وتوزيع الملمس داخل الشكل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// تطبيق محاذاة الملمس على تعبئة الشكل.
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// استخدم خيار التوافق لتحديد الشكل باستخدام DML إذا كنت تريد الحصول على "TextureAlignment"
//الخاصية بعد حفظ المستند.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);

doc = new Document(ArtifactsDir + "Shape.TextureFill.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(TextureAlignment.TopRight, shape.Fill.TextureAlignment);
Assert.AreEqual(PresetTexture.Canvas, shape.Fill.PresetTexture);
```

### أنظر أيضا

* enum [PresetTexture](../../presettexture/)
* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
