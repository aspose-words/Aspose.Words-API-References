---
title: Fill.TextureAlignment
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words لـ .NET
description: عيّن خاصية TextureAlignment لتحسين تعبئة نسيج البلاط. خصّص المحاذاة بسهولة لتحسين المظهر ودقة التصميم.
type: docs
weight: 190
url: /ar/net/aspose.words.drawing/fill/texturealignment/
---
## Fill.TextureAlignment property

يحصل على محاذاة تعبئة نسيج البلاط أو يعينها.

```csharp
public TextureAlignment TextureAlignment { get; set; }
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

* enum [TextureAlignment](../../texturealignment/)
* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
