---
title: RelativeHorizontalPosition Enum
linktitle: RelativeHorizontalPosition
articleTitle: RelativeHorizontalPosition
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.RelativeHorizontalPosition تعداد. يحدد الموضع الأفقي للشكل أو إطار النص النسبي في C#.
type: docs
weight: 1190
url: /ar/net/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enumeration

يحدد الموضع الأفقي للشكل أو إطار النص النسبي.

```csharp
public enum RelativeHorizontalPosition
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Margin | `0` | يحدد أن الموضع الأفقي يجب أن يكون متناسبًا مع هوامش الصفحة. |
| Page | `1` | تم وضع الكائن بالنسبة إلى الحافة اليسرى للصفحة. |
| Column | `2` | تم وضع الكائن بالنسبة إلى الجانب الأيسر من العمود. |
| Character | `3` | تم وضع الكائن بالنسبة إلى الجانب الأيسر من الفقرة. |
| LeftMargin | `4` | يحدد أن الموضع الأفقي يجب أن يكون متناسبًا مع الهامش الأيسر للصفحة. |
| RightMargin | `5` | يحدد أن الموضع الأفقي يجب أن يكون متناسبًا مع الهامش الأيمن للصفحة. |
| InsideMargin | `6` | يحدد أن الموضع الأفقي يجب أن يكون متناسبًا مع الهامش الداخلي للصفحة الحالية (الهامش الأيسر في الصفحات الفردية، والهامش الأيمن في الصفحات الزوجية). |
| OutsideMargin | `7` | يحدد أن الموضع الأفقي يجب أن يكون متناسبًا مع الهامش الخارجي للصفحة الحالية (الهامش الأيمن في الصفحات الفردية، والهامش الأيسر في الصفحات الزوجية). |
| Default | `2` | القيمة الافتراضية هيColumn . |

## أمثلة

يوضح كيفية إدراج صورة عائمة في وسط الصفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل صورة عائمة ستظهر خلف النص المتداخل وقم بمحاذاتها مع منتصف الصفحة.
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

// أدخل الصورة في الرأس بحيث تكون مرئية في كل صفحة.
Image image = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(image);
shape.WrapType = WrapType.None;
shape.BehindText = true;

// ضع الصورة في وسط الصفحة.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

يوضح كيفية إدراج صورة واستخدامها كعلامة مائية (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل الصورة في الرأس بحيث تكون مرئية في كل صفحة.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

using (SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png"))
{
    builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
    Shape shape = builder.InsertImage(image);
    shape.WrapType = WrapType.None;
    shape.BehindText = true;

    // ضع الصورة في وسط الصفحة.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
    shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
    shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
    shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermarkNetStandard2.docx");
```

### أنظر أيضا

* property [RelativeHorizontalPosition](../shapebase/relativehorizontalposition/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
