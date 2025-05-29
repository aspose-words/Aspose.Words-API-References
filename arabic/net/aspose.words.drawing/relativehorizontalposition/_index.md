---
title: RelativeHorizontalPosition Enum
linktitle: RelativeHorizontalPosition
articleTitle: RelativeHorizontalPosition
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Drawing.RelativeHorizontalPosition enum لتحديد الموضع الأفقي الدقيق للأشكال وإطارات النص في مستنداتك.
type: docs
weight: 1580
url: /ar/net/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enumeration

يحدد ما هو الموضع الأفقي لإطار الشكل أو النص بالنسبة إليه.

```csharp
public enum RelativeHorizontalPosition
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Margin | `0` | يحدد أن الوضع الأفقي يجب أن يكون نسبيًا إلى هوامش الصفحة. |
| Page | `1` | يتم وضع الكائن بالنسبة للحافة اليسرى للصفحة. |
| Column | `2` | يتم وضع الكائن بالنسبة إلى الجانب الأيسر من العمود. |
| Character | `3` | يتم وضع الكائن بالنسبة إلى الجانب الأيسر من الفقرة. |
| LeftMargin | `4` | يحدد أن الوضع الأفقي يجب أن يكون نسبيًا إلى الهامش الأيسر للصفحة. |
| RightMargin | `5` | يحدد أن الوضع الأفقي يجب أن يكون نسبيًا إلى الهامش الأيمن للصفحة. |
| InsideMargin | `6` | يحدد أن الوضع الأفقي يجب أن يكون نسبيًا إلى الهامش الداخلي للصفحة الحالية (الهامش الأيسر في الصفحات الفردية، والهامش الأيمن في الصفحات الزوجية). |
| OutsideMargin | `7` | يحدد أن الوضع الأفقي يجب أن يكون نسبيًا إلى الهامش الخارجي للصفحة الحالية (الهامش الأيمن في الصفحات الفردية، والهامش الأيسر في الصفحات الزوجية). |
| Default | `2` | القيمة الافتراضية هيColumn . |

## أمثلة

يوضح كيفية إدراج صورة عائمة في وسط الصفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج صورة عائمة ستظهر خلف النص المتداخل وقم بمحاذاتها مع مركز الصفحة.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

يوضح كيفية إدراج صورة واستخدامها كعلامة مائية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//أدرج الصورة في الرأس حتى تكون مرئية في كل صفحة.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

// ضع الصورة في وسط الصفحة.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

### أنظر أيضا

* property [RelativeHorizontalPosition](../shapebase/relativehorizontalposition/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
