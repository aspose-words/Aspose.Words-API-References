---
title: RelativeVerticalPosition Enum
linktitle: RelativeVerticalPosition
articleTitle: RelativeVerticalPosition
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.RelativeVerticalPosition تعداد. يحدد الموضع الرأسي للشكل أو إطار النص النسبي في C#.
type: docs
weight: 1210
url: /ar/net/aspose.words.drawing/relativeverticalposition/
---
## RelativeVerticalPosition enumeration

يحدد الموضع الرأسي للشكل أو إطار النص النسبي.

```csharp
public enum RelativeVerticalPosition
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Margin | `0` | يحدد أن الموضع الرأسي يجب أن يكون متناسبًا مع هوامش الصفحة. |
| Page | `1` | تم وضع الكائن بالنسبة إلى الحافة العلوية للصفحة. |
| Paragraph | `2` | يتم وضع الكائن بالنسبة إلى أعلى الفقرة التي تحتوي على نقطة الارتساء. |
| Line | `3` | غير موثقة. |
| TopMargin | `4` | يحدد أن الموضع الرأسي يجب أن يكون متناسبًا مع الهامش العلوي للصفحة الحالية. |
| BottomMargin | `5` | يحدد أن الموضع الرأسي يجب أن يكون متناسبًا مع الهامش السفلي للصفحة الحالية. |
| InsideMargin | `6` | يحدد أن الموضع الرأسي يجب أن يكون متناسبًا مع الهامش الداخلي للصفحة الحالية. |
| OutsideMargin | `7` | يحدد أن الموضع الرأسي يجب أن يكون متناسبًا مع الهامش الخارجي للصفحة الحالية. |
| TableDefault | `0` | القيمة الافتراضية هيMargin . |
| TextFrameDefault | `2` | القيمة الافتراضية هيParagraph . |

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

* property [RelativeVerticalPosition](../shapebase/relativeverticalposition/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
