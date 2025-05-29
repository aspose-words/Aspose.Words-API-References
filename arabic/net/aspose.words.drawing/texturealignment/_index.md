---
title: TextureAlignment Enum
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Drawing.TextureAlignment enum لمحاذاة دقيقة لملء الملمس. حسّن تصميمات مستنداتك مع خيارات تبليط سلسة!
type: docs
weight: 1780
url: /ar/net/aspose.words.drawing/texturealignment/
---
## TextureAlignment enumeration

يحدد محاذاة بلاط تعبئة الملمس.

```csharp
public enum TextureAlignment
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| TopLeft | `0` | محاذاة الملمس في أعلى اليسار. |
| Top | `1` | محاذاة الملمس العلوي. |
| TopRight | `2` | محاذاة الملمس في أعلى اليمين. |
| Left | `3` | محاذاة الملمس إلى اليسار. |
| Center | `4` | محاذاة الملمس المركزي. |
| Right | `5` | محاذاة الملمس إلى اليمين. |
| BottomLeft | `6` | محاذاة الملمس في أسفل اليسار. |
| Bottom | `7` | محاذاة الملمس السفلي. |
| BottomRight | `8` | محاذاة الملمس في أسفل اليمين. |
| None | `9` | لا يوجد محاذاة للملمس. |

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

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
