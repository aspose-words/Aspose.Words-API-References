---
title: PageSetup.PageWidth
second_title: Aspose.Words لمراجع .NET API
description: PageSetup ملكية. إرجاع أو تحديد عرض الصفحة بالنقاط.
type: docs
weight: 330
url: /ar/net/aspose.words/pagesetup/pagewidth/
---
## PageSetup.PageWidth property

إرجاع أو تحديد عرض الصفحة بالنقاط.

```csharp
public double PageWidth { get; set; }
```

### أمثلة

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

يوضح كيفية إدراج صورة عائمة ، وتحديد موضعها وحجمها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// تكوين خاصية "RelativeHorizontalPosition" للشكل لمعالجة قيمة الخاصية "Left"
 // كمسافة أفقية للشكل ، بالنقاط ، من الجانب الأيسر للصفحة.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// اضبط المسافة الأفقية للشكل من الجانب الأيسر للصفحة على 100.
shape.Left = 100;

// استخدم خاصية "RelativeVerticalPosition" بطريقة مماثلة لوضع الشكل 80 نقطة أسفل أعلى الصفحة.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// قم بتعيين ارتفاع الشكل ، والذي سيقيس العرض تلقائيًا للحفاظ على الأبعاد.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// تحتوي خصائص "الجزء السفلي" و "الأيمن" على الحواف السفلية واليمنى للصورة.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../pagesetup/)
* المجسم [Aspose.Words](../../../)


