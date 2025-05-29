---
title: TextBox Class
linktitle: TextBox
articleTitle: TextBox
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.TextBox لتخصيص عرض النص بسهولة داخل الأشكال، مما يعزز الجاذبية البصرية والوظائف للمستند الخاص بك.
type: docs
weight: 1730
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
| [InternalMarginLeft](../../aspose.words.drawing/textbox/internalmarginleft/) { get; set; } | يحدد الهامش الداخلي الأيسر بالنقاط للشكل. |
| [InternalMarginRight](../../aspose.words.drawing/textbox/internalmarginright/) { get; set; } | يحدد الهامش الداخلي الأيمن بالنقاط للشكل. |
| [InternalMarginTop](../../aspose.words.drawing/textbox/internalmargintop/) { get; set; } | يحدد الهامش العلوي الداخلي بالنقاط للشكل. |
| [LayoutFlow](../../aspose.words.drawing/textbox/layoutflow/) { get; set; } | يحدد تدفق تخطيط النص في الشكل. |
| [Next](../../aspose.words.drawing/textbox/next/) { get; set; } | يعيد أو يعين`TextBox` الذي يمثل التالي`TextBox`في تسلسل من الأشكال. |
| [NoTextRotation](../../aspose.words.drawing/textbox/notextrotation/) { get; set; } | يحصل على قيمة منطقية أو يعينها تشير إلى أنه لا ينبغي تدوير نص مربع النص عند تدوير الشكل. |
| [Parent](../../aspose.words.drawing/textbox/parent/) { get; } | يحصل على شكل رئيسي لـ`TextBox` . |
| [Previous](../../aspose.words.drawing/textbox/previous/) { get; } | يعيد`TextBox` الذي يمثل السابق`TextBox`في تسلسل من الأشكال. |
| [TextBoxWrapMode](../../aspose.words.drawing/textbox/textboxwrapmode/) { get; set; } | يحدد كيفية التفاف النص داخل الشكل. |
| [VerticalAnchor](../../aspose.words.drawing/textbox/verticalanchor/) { get; set; } | يحدد المحاذاة الرأسية للنص داخل الشكل. |

## طُرق

| اسم | وصف |
| --- | --- |
| [BreakForwardLink](../../aspose.words.drawing/textbox/breakforwardlink/)() | يقطع الرابط إلى التالي`TextBox` . |
| [IsValidLinkTarget](../../aspose.words.drawing/textbox/isvalidlinktarget/)(*TextBox*) | يحدد ما إذا كان هذا`TextBox` يمكن ربطها بالهدف`TextBox` . |

## ملاحظات

استخدم[`TextBox`](../shape/textbox/) الخاصية للوصول إلى خصائص النص الخاصة بالشكل. لا تقم بإنشاء مثيلات من`TextBox` الصف مباشرة.

## أمثلة

يوضح كيفية تعيين الهوامش الداخلية لمربع النص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//إدراج مربع نص آخر بهوامش محددة.
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

يوضح كيفية تعيين اتجاه النص داخل مربع النص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// انقل منشئ المستندات إلى داخل مربع النص وأضف نصًا.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// قم بتعيين خاصية "LayoutFlow" لتعيين اتجاه محتويات النص في مربع النص هذا.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

يوضح كيفية تغيير حجم مربع النص ليتناسب مع محتوياته بشكل محكم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// قم بتطبيق هذه القيم على كلا هذين العنصرين للحصول على الشكل الرئيسي المناسب
// بإحكام حول محتويات النص، متجاهلاً الأبعاد التي حددناها.
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
