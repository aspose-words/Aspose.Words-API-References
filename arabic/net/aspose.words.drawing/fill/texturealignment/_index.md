---
title: Fill.TextureAlignment
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words لـ .NET
description: Fill TextureAlignment ملكية. الحصول على أو تعيين المحاذاة لملء نسيج التجانب في C#.
type: docs
weight: 180
url: /ar/net/aspose.words.drawing/fill/texturealignment/
---
## Fill.TextureAlignment property

الحصول على أو تعيين المحاذاة لملء نسيج التجانب.

```csharp
public TextureAlignment TextureAlignment { get; set; }
```

## أمثلة

يوضح كيفية تعبئة وتبليط النسيج داخل الشكل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// تطبيق محاذاة النسيج على تعبئة الشكل.
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// استخدم خيار الامتثال لتحديد الشكل باستخدام DML إذا كنت تريد الحصول على "TextureAlignment"
// الخاصية بعد حفظ المستند.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);
```

### أنظر أيضا

* enum [TextureAlignment](../../texturealignment/)
* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
