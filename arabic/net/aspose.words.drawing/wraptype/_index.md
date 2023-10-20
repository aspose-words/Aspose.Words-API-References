---
title: WrapType Enum
linktitle: WrapType
articleTitle: WrapType
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.WrapType تعداد. يحدد كيفية التفاف النص حول الشكل أو الصورة في C#.
type: docs
weight: 1400
url: /ar/net/aspose.words.drawing/wraptype/
---
## WrapType enumeration

يحدد كيفية التفاف النص حول الشكل أو الصورة.

```csharp
public enum WrapType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `3` | لا يوجد نص يلتف حول الشكل. يتم وضع الشكل خلف النص أو أمامه. |
| Inline | `0` | يبقى الشكل على نفس طبقة النص ويتم التعامل معه كحرف. |
| TopBottom | `1` | يتوقف النص عند أعلى الشكل ثم يبدأ من جديد على السطر الموجود أسفل الشكل. |
| Square | `2` | يلتف النص حول جميع جوانب المربع المحيط بالشكل. |
| Tight | `4` | يتم الالتفاف بإحكام حول حواف الشكل، بدلاً من الالتفاف حول المربع المحيط. |
| Through | `5` | نفس الشكل الضيق، ولكنه يلتف داخل أي أجزاء مفتوحة من الشكل. |

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

* property [WrapType](../shapebase/wraptype/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
