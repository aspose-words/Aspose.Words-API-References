---
title: DocumentBuilder.MoveToHeaderFooter
linktitle: MoveToHeaderFooter
articleTitle: MoveToHeaderFooter
second_title: Aspose.Words لـ .NET
description: انتقل بسهولة إلى الرؤوس والتذييلات باستخدام طريقة MoveToHeaderFooter في DocumentBuilder، مما يعزز كفاءة تحرير المستندات لديك.
type: docs
weight: 580
url: /ar/net/aspose.words/documentbuilder/movetoheaderfooter/
---
## DocumentBuilder.MoveToHeaderFooter method

يحرك المؤشر إلى بداية الرأس أو التذييل في القسم الحالي.

```csharp
public void MoveToHeaderFooter(HeaderFooterType headerFooterType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| headerFooterType | HeaderFooterType | يحدد الرأس أو التذييل الذي سيتم الانتقال إليه. |

## ملاحظات

بعد نقل المؤشر إلى الرأس أو التذييل، يمكنك استخدام الباقي[`DocumentBuilder`](../) طرق لتعديل محتويات الرأس أو التذييل.

إذا كنت تريد إنشاء رؤوس وتذييلات مختلفة للصفحة الأولى، فستحتاج إلى لتعيين[`DifferentFirstPageHeaderFooter`](../../pagesetup/differentfirstpageheaderfooter/).

إذا كنت تريد إنشاء رؤوس وتذييلات مختلفة للصفحات الفردية والزوجية، فستحتاج إلى تعيين x000d_[`OddAndEvenPagesHeaderFooter`](../../pagesetup/oddandevenpagesheaderfooter/).

يستخدم[`MoveToSection`](../movetosection/) للانتقال من العنوان إلى النص الرئيسي.

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

يوضح كيفية إنشاء الرؤوس والتذييلات في مستند باستخدام DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// حدد أننا نريد رؤوسًا وتذييلات مختلفة للصفحات الأولى والزوجية والفردية.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// قم بإنشاء الرؤوس، ثم أضف ثلاث صفحات إلى المستند لعرض كل نوع من أنواع الرؤوس.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

### أنظر أيضا

* enum [HeaderFooterType](../../headerfootertype/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
