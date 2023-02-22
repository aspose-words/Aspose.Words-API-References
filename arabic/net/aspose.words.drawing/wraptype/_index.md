---
title: Enum WrapType
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.WrapType تعداد. يحدد كيفية التفاف النص حول شكل أو صورة.
type: docs
weight: 1250
url: /ar/net/aspose.words.drawing/wraptype/
---
## WrapType enumeration

يحدد كيفية التفاف النص حول شكل أو صورة.

```csharp
public enum WrapType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `3` | لا يوجد نص يلتف حول الشكل. يوضع الشكل خلف النص أو أمامه. |
| Inline | `0` | يظل الشكل على نفس طبقة النص ويتم التعامل معه كحرف. |
| TopBottom | `1` | يتوقف النص في أعلى الشكل ويعاد تشغيله على السطر الموجود أسفل الشكل. |
| Square | `2` | يلتف النص حول جميع جوانب المربع المحيط بالشكل. |
| Tight | `4` | يلتف بإحكام حول حواف الشكل ، بدلاً من الالتفاف حول المربع المحيط. |
| Through | `5` | مثل ضيق ، لكنه يلتف داخل أي جزء من الشكل المفتوح. |

### أمثلة

يوضح كيفية إدراج صورة عائمة في وسط الصفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل صورة عائمة ستظهر خلف النص المتداخل وقم بمحاذاة مركز الصفحة.
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

// ضع الصورة في منتصف الصفحة.
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

    // ضع الصورة في منتصف الصفحة.
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


