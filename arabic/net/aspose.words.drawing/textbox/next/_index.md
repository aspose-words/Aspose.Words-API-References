---
title: TextBox.Next
linktitle: Next
articleTitle: Next
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية TextBox Next على تعزيز سير عمل التصميم الخاص بك عن طريق ربط TextBoxes بسلاسة في مشاريعك لتحسين التنظيم.
type: docs
weight: 70
url: /ar/net/aspose.words.drawing/textbox/next/
---
## TextBox.Next property

يعيد أو يعين[`TextBox`](../) الذي يمثل التالي[`TextBox`](../)في تسلسل من الأشكال.

```csharp
public TextBox Next { get; set; }
```

## أمثلة

يوضح كيفية ربط مربعات النص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape1 = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox1 = textBoxShape1.TextBox;
builder.Writeln();

Shape textBoxShape2 = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox2 = textBoxShape2.TextBox;
builder.Writeln();

Shape textBoxShape3 = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox3 = textBoxShape3.TextBox;
builder.Writeln();

Shape textBoxShape4 = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox4 = textBoxShape4.TextBox;

// إنشاء روابط بين بعض مربعات النص.
if (textBox1.IsValidLinkTarget(textBox2))
    textBox1.Next = textBox2;

if (textBox2.IsValidLinkTarget(textBox3))
    textBox2.Next = textBox3;

// فقط مربع النص الفارغ يمكن أن يحتوي على رابط.
Assert.True(textBox3.IsValidLinkTarget(textBox4));

builder.MoveTo(textBoxShape4.LastParagraph);
builder.Write("Hello world!");

Assert.False(textBox3.IsValidLinkTarget(textBox4));

if (textBox1.Next != null && textBox1.Previous == null)
    Console.WriteLine("This TextBox is the head of the sequence");

if (textBox2.Next != null && textBox2.Previous != null)
    Console.WriteLine("This TextBox is the middle of the sequence");

if (textBox3.Next == null && textBox3.Previous != null)
{
    Console.WriteLine("This TextBox is the tail of the sequence");

    // قم بقطع الارتباط الأمامي بين textBox2 وtextBox3، ثم تأكد من عدم وجود ارتباط بينهما بعد الآن.
    textBox3.Previous.BreakForwardLink();
    Assert.IsTrue(textBox2.Next == null);
    Assert.IsTrue(textBox3.Previous == null);
}

doc.Save(ArtifactsDir + "Shape.CreateLinkBetweenTextBoxes.docx");
```

### أنظر أيضا

* class [TextBox](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
