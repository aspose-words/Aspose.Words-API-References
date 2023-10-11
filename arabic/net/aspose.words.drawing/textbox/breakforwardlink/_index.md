---
title: TextBox.BreakForwardLink
second_title: Aspose.Words لمراجع .NET API
description: TextBox طريقة. يقطع الرابط إلى التاليTextBox .
type: docs
weight: 130
url: /ar/net/aspose.words.drawing/textbox/breakforwardlink/
---
## TextBox.BreakForwardLink method

يقطع الرابط إلى التالي[`TextBox`](../) .

```csharp
public void BreakForwardLink()
```

### ملاحظات

`BreakForwardLink`لا يؤدي إلى قطع جميع الروابط الأخرى في التسلسل الحالي للأشكال. على سبيل المثال: تسلسل 1-2-3-4 و`BreakForwardLink` في مربع النص الثاني سيتم إنشاء تسلسلين 1-2، 3-4.

### أمثلة

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

// قد يحتوي مربع النص الفارغ فقط على رابط.
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

    // اقطع الارتباط الأمامي بين textBox2 وtextBox3، ثم تحقق من أنهما لم يعودا مرتبطين.
    textBox3.Previous.BreakForwardLink();

    Assert.IsTrue(textBox2.Next == null);
    Assert.IsTrue(textBox3.Previous == null);
}

doc.Save(ArtifactsDir + "Shape.CreateLinkBetweenTextBoxes.docx");
```

### أنظر أيضا

* class [TextBox](../)
* مساحة الاسم [Aspose.Words.Drawing](../../textbox/)
* المجسم [Aspose.Words](../../../)


