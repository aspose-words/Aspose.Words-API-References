---
title: TextBoxAnchor Enum
linktitle: TextBoxAnchor
articleTitle: TextBoxAnchor
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.TextBoxAnchor تعداد. يحدد القيم المستخدمة للمحاذاة العمودية لنص الشكل في C#.
type: docs
weight: 1330
url: /ar/net/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enumeration

يحدد القيم المستخدمة للمحاذاة العمودية لنص الشكل.

```csharp
public enum TextBoxAnchor
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Top | `0` | تتم محاذاة النص إلى أعلى مربع النص. |
| Middle | `1` | تتم محاذاة النص إلى منتصف مربع النص. |
| Bottom | `2` | تتم محاذاة النص إلى أسفل مربع النص. |
| TopCentered | `3` | تتم محاذاة النص إلى أعلى منتصف مربع النص. |
| MiddleCentered | `4` | تتم محاذاة النص إلى منتصف مربع النص. |
| BottomCentered | `5` | تتم محاذاة النص إلى الجزء السفلي الأوسط من مربع النص. |
| TopBaseline | `6` | تتم محاذاة النص إلى الخط الأساسي العلوي لمربع النص. |
| BottomBaseline | `7` | تتم محاذاة النص إلى الخط الأساسي السفلي لمربع النص. |
| TopCenteredBaseline | `8` | تتم محاذاة النص إلى الخط الأساسي الأوسط العلوي لمربع النص. |
| BottomCenteredBaseline | `9` | تتم محاذاة النص إلى الخط الأساسي الأوسط السفلي لمربع النص. |

## أمثلة

يوضح كيفية محاذاة محتويات النص في مربع النص عموديًا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// قم بتعيين خاصية "VerticalAnchor" على "TextBoxAnchor.Top" إلى
// قم بمحاذاة النص الموجود في مربع النص هذا مع الجانب العلوي من الشكل.
// قم بتعيين خاصية "VerticalAnchor" على "TextBoxAnchor.Middle" إلى
// قم بمحاذاة النص الموجود في مربع النص هذا إلى منتصف الشكل.
// قم بتعيين خاصية "VerticalAnchor" على "TextBoxAnchor.Bottom" إلى
// قم بمحاذاة النص الموجود في مربع النص هذا إلى أسفل الشكل.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// المحاذاة الرأسية للنص داخل مربعات النص متاحة بدءًا من Microsoft Word 2007 وما بعده.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
