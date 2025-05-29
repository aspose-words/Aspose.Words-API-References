---
title: RelativeVerticalPosition Enum
linktitle: RelativeVerticalPosition
articleTitle: RelativeVerticalPosition
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Drawing.RelativeVerticalPosition لتحديد الوضع الرأسي للأشكال وإطارات النص بشكل فعال وتحسين تخطيطات المستندات.
type: docs
weight: 1600
url: /ar/net/aspose.words.drawing/relativeverticalposition/
---
## RelativeVerticalPosition enumeration

يحدد ما هو الموضع الرأسي لإطار الشكل أو النص بالنسبة إليه.

```csharp
public enum RelativeVerticalPosition
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Margin | `0` | يحدد أن الوضع الرأسي يجب أن يكون نسبيًا إلى هوامش الصفحة. |
| Page | `1` | يتم وضع الكائن بالنسبة للحافة العلوية للصفحة. |
| Paragraph | `2` | يتم وضع الكائن بالنسبة إلى الجزء العلوي من الفقرة التي تحتوي على المرساة. |
| Line | `3` | غير موثق. |
| TopMargin | `4` | يحدد أن الوضع الرأسي يجب أن يكون نسبيًا إلى الهامش العلوي للصفحة الحالية. |
| BottomMargin | `5` | يحدد أن الوضع الرأسي يجب أن يكون نسبيًا إلى الهامش السفلي للصفحة الحالية. |
| InsideMargin | `6` | يحدد أن الوضع الرأسي يجب أن يكون نسبيًا إلى الهامش الداخلي للصفحة الحالية. |
| OutsideMargin | `7` | يحدد أن الوضع الرأسي يجب أن يكون نسبيًا إلى الهامش الخارجي للصفحة الحالية. |
| TableDefault | `0` | القيمة الافتراضية هيMargin |
| TextFrameDefault | `2` | القيمة الافتراضية هيParagraph |

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

* property [RelativeVerticalPosition](../shapebase/relativeverticalposition/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
