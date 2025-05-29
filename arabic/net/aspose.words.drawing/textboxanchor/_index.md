---
title: TextBoxAnchor Enum
linktitle: TextBoxAnchor
articleTitle: TextBoxAnchor
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.Drawing.TextBoxAnchor لمحاذاة نص الشكل عموديًا بدقة. حسّن تنسيق مستندك بسهولة!
type: docs
weight: 1740
url: /ar/net/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enumeration

يحدد القيم المستخدمة لمحاذاة نص الشكل عموديًا.

```csharp
public enum TextBoxAnchor
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Top | `0` | تم محاذاة النص إلى أعلى مربع النص. |
| Middle | `1` | تم محاذاة النص إلى منتصف مربع النص. |
| Bottom | `2` | تم محاذاة النص إلى أسفل مربع النص. |
| TopCentered | `3` | يتم محاذاة النص إلى الجزء العلوي الأوسط من مربع النص. |
| MiddleCentered | `4` | يتم محاذاة النص إلى منتصف مربع النص. |
| BottomCentered | `5` | يتم محاذاة النص إلى أسفل وسط مربع النص. |
| TopBaseline | `6` | يتم محاذاة النص إلى خط الأساس العلوي لمربع النص. |
| BottomBaseline | `7` | يتم محاذاة النص مع خط الأساس السفلي لمربع النص. |
| TopCenteredBaseline | `8` | يتم محاذاة النص مع خط الأساس المركزي العلوي لمربع النص. |
| BottomCenteredBaseline | `9` | يتم محاذاة النص مع خط الأساس المركزي السفلي لمربع النص. |

## أمثلة

يوضح كيفية محاذاة محتويات النص في مربع النص عموديًا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// اضبط خاصية "VerticalAnchor" على "TextBoxAnchor.Top" لـ
// قم بمحاذاة النص الموجود في مربع النص هذا مع الجانب العلوي للشكل.
// اضبط خاصية "VerticalAnchor" على "TextBoxAnchor.Middle"
// محاذاة النص في مربع النص هذا إلى مركز الشكل.
// اضبط خاصية "VerticalAnchor" على "TextBoxAnchor.Bottom" لـ
// قم بمحاذاة النص الموجود في مربع النص هذا إلى أسفل الشكل.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// أصبحت المحاذاة الرأسية للنص داخل مربعات النص متاحة من Microsoft Word 2007 فصاعدًا.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
