---
title: PageSetup.PageWidth
linktitle: PageWidth
articleTitle: PageWidth
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PageWidth في PageSetup لضبط عرض الصفحة بالنقاط بسهولة، مما يعزز تخطيط المستند الخاص بك للحصول على عرض مثالي.
type: docs
weight: 340
url: /ar/net/aspose.words/pagesetup/pagewidth/
---
## PageSetup.PageWidth property

يعيد أو يضبط عرض الصفحة بالنقاط.

```csharp
public double PageWidth { get; set; }
```

## أمثلة

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

يوضح كيفية إدراج صورة عائمة وتحديد موضعها وحجمها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// قم بتكوين خاصية "RelativeHorizontalPosition" الخاصة بالشكل لمعالجة قيمة خاصية "Left"
 // كمسافة أفقية للشكل، بالنقاط، من الجانب الأيسر للصفحة.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// قم بتعيين المسافة الأفقية للشكل من الجانب الأيسر للصفحة إلى 100.
shape.Left = 100;

// استخدم خاصية "RelativeVerticalPosition" بطريقة مماثلة لوضع الشكل على مسافة 80 نقطة أسفل الجزء العلوي من الصفحة.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// قم بتعيين ارتفاع الشكل، والذي سيقوم تلقائيًا بتغيير العرض للحفاظ على الأبعاد.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// تحتوي خصائص "الأسفل" و"اليمين" على الحواف السفلية واليمنى للصورة.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
