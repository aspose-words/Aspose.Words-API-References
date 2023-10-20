---
title: TextBox Class
linktitle: TextBox
articleTitle: TextBox
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.TextBox فصل. يحدد السمات التي تحدد كيفية عرض النص داخل الشكل في C#.
type: docs
weight: 1320
url: /ar/net/aspose.words.drawing/textbox/
---
## TextBox class

يحدد السمات التي تحدد كيفية عرض النص داخل الشكل.

لمعرفة المزيد، قم بزيارة[العمل مع الأشكال](https://docs.aspose.com/words/net/working-with-shapes/) مقالة توثيقية.

```csharp
public class TextBox
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [FitShapeToText](../../aspose.words.drawing/textbox/fitshapetotext/) { get; set; } | يحدد ما إذا كان Microsoft Word سيقوم بتكبير الشكل ليناسب النص. |
| [InternalMarginBottom](../../aspose.words.drawing/textbox/internalmarginbottom/) { get; set; } | يحدد الهامش السفلي الداخلي بالنقاط للشكل. |
| [InternalMarginLeft](../../aspose.words.drawing/textbox/internalmarginleft/) { get; set; } | يحدد الهامش الأيسر الداخلي بالنقاط للشكل. |
| [InternalMarginRight](../../aspose.words.drawing/textbox/internalmarginright/) { get; set; } | يحدد الهامش الأيمن الداخلي بالنقاط للشكل. |
| [InternalMarginTop](../../aspose.words.drawing/textbox/internalmargintop/) { get; set; } | يحدد الهامش العلوي الداخلي بالنقاط للشكل. |
| [LayoutFlow](../../aspose.words.drawing/textbox/layoutflow/) { get; set; } | تحديد تدفق تخطيط النص في الشكل. |
| [Next](../../aspose.words.drawing/textbox/next/) { get; set; } | إرجاع أو تعيين أ`TextBox` الذي يمثل القادم`TextBox` في تسلسل من الأشكال. |
| [NoTextRotation](../../aspose.words.drawing/textbox/notextrotation/) { get; set; } | الحصول على قيمة منطقية أو تعيينها تشير إلى عدم تدوير نص مربع النص عند تدوير الشكل. |
| [Parent](../../aspose.words.drawing/textbox/parent/) { get; } | يحصل على الشكل الأصلي لـ`TextBox` . |
| [Previous](../../aspose.words.drawing/textbox/previous/) { get; } | إرجاع أ`TextBox` الذي يمثل السابق`TextBox` في تسلسل من الأشكال. |
| [TextBoxWrapMode](../../aspose.words.drawing/textbox/textboxwrapmode/) { get; set; } | يحدد كيفية التفاف النص داخل الشكل. |
| [VerticalAnchor](../../aspose.words.drawing/textbox/verticalanchor/) { get; set; } | يحدد المحاذاة الرأسية للنص داخل الشكل. |

## طُرق

| اسم | وصف |
| --- | --- |
| [BreakForwardLink](../../aspose.words.drawing/textbox/breakforwardlink/)() | يقطع الرابط إلى التالي`TextBox` . |
| [IsValidLinkTarget](../../aspose.words.drawing/textbox/isvalidlinktarget/)(*TextBox*) | يحدد ما إذا كان هذا`TextBox` يمكن ربطها بالهدف`TextBox` . |

## ملاحظات

استخدم ال[`TextBox`](../shape/textbox/) الخاصية للوصول إلى خصائص النص الخاصة بالشكل. لا تقم بإنشاء مثيلات للشكل`TextBox` الصف مباشرة.

## أمثلة

يوضح كيفية تعيين الهوامش الداخلية لمربع النص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل مربع نص آخر بهوامش محددة.
Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox = textBoxShape.TextBox;
textBox.InternalMarginTop = 15;
textBox.InternalMarginBottom = 15;
textBox.InternalMarginLeft = 15;
textBox.InternalMarginRight = 15;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text placed according to textbox margins.");

doc.Save(ArtifactsDir + "Shape.TextBoxMargins.docx");
```

يوضح كيفية ضبط اتجاه النص داخل مربع النص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// انقل أداة إنشاء المستندات إلى داخل TextBox وأضف نصًا.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// قم بتعيين خاصية "LayoutFlow" لتعيين اتجاه لمحتويات النص في مربع النص هذا.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

يوضح كيفية جعل مربع النص يغير حجمه ليناسب محتوياته بإحكام.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// قم بتطبيق هذه القيم على هذين العضوين للحصول على الشكل الأصلي المناسب
// يحيط بإحكام بمحتويات النص، متجاهلاً الأبعاد التي وضعناها.
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
