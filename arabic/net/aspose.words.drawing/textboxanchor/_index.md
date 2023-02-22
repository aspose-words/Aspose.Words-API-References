---
title: Enum TextBoxAnchor
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.TextBoxAnchor تعداد. تحديد القيم المستخدمة للمحاذاة الرأسية لنص الشكل.
type: docs
weight: 1180
url: /ar/net/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enumeration

تحديد القيم المستخدمة للمحاذاة الرأسية لنص الشكل.

```csharp
public enum TextBoxAnchor
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Top | `0` | تمت محاذاة النص إلى أعلى مربع النص. |
| Middle | `1` | يتم محاذاة النص إلى منتصف مربع النص. |
| Bottom | `2` | تمت محاذاة النص إلى أسفل مربع النص. |
| TopCentered | `3` | تتم محاذاة النص إلى منتصف مربع النص العلوي. |
| MiddleCentered | `4` | يتم محاذاة النص إلى منتصف مربع النص. |
| BottomCentered | `5` | تتم محاذاة النص إلى أسفل منتصف مربع النص. |
| TopBaseline | `6` | تمت محاذاة النص إلى خط الأساس العلوي لمربع النص. |
| BottomBaseline | `7` | تتم محاذاة النص إلى خط الأساس السفلي لمربع النص. |
| TopCenteredBaseline | `8` | تتم محاذاة النص إلى خط الأساس العلوي الأوسط لمربع النص. |
| BottomCenteredBaseline | `9` | تتم محاذاة النص إلى خط الأساس السفلي المركزي لمربع النص. |

### أمثلة

يوضح كيفية محاذاة محتويات النص لمربع نص عموديًا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// قم بتعيين خاصية "VerticalAnchor" على "TextBoxAnchor.Top" إلى
// محاذاة النص في مربع النص هذا مع الجانب العلوي للشكل.
// اضبط خاصية "VerticalAnchor" على "TextBoxAnchor.Middle" على
// محاذاة النص في مربع النص هذا إلى وسط الشكل.
// قم بتعيين خاصية "VerticalAnchor" على "TextBoxAnchor.Bottom" إلى
// محاذاة النص في مربع النص هذا إلى أسفل الشكل.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// المحاذاة الرأسية للنص داخل مربعات النص متاحة من Microsoft Word 2007 وما بعده.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)


