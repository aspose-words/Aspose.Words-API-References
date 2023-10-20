---
title: TextBox.BreakForwardLink
linktitle: BreakForwardLink
articleTitle: BreakForwardLink
second_title: Aspose.Words för .NET
description: TextBox BreakForwardLink metod. Bryter länken till nästaTextBox  i C#.
type: docs
weight: 130
url: /sv/net/aspose.words.drawing/textbox/breakforwardlink/
---
## TextBox.BreakForwardLink method

Bryter länken till nästa[`TextBox`](../) .

```csharp
public void BreakForwardLink()
```

## Anmärkningar

`BreakForwardLink`bryter inte alla andra länkar i den aktuella sekvensen av former. Till exempel: 1-2-3-4 sekvens och`BreakForwardLink` vid den andra textrutan kommer att skapa två sekvenser 1-2, 3-4.

## Exempel

Visar hur man länkar textrutor.

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

// Skapa länkar mellan några av textrutorna.
if (textBox1.IsValidLinkTarget(textBox2))
    textBox1.Next = textBox2;

if (textBox2.IsValidLinkTarget(textBox3))
    textBox2.Next = textBox3;

// Endast en tom textruta kan ha en länk.
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

    // Bryt framåtlänken mellan textBox2 och textBox3 och verifiera sedan att de inte längre är länkade.
    textBox3.Previous.BreakForwardLink();

    Assert.IsTrue(textBox2.Next == null);
    Assert.IsTrue(textBox3.Previous == null);
}

doc.Save(ArtifactsDir + "Shape.CreateLinkBetweenTextBoxes.docx");
```

### Se även

* class [TextBox](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
