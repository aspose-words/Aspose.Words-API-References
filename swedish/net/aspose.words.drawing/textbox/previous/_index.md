---
title: TextBox.Previous
linktitle: Previous
articleTitle: Previous
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Föregående textruta och få enkel åtkomst till den föregående textrutan i din formsekvens för en effektiv design och ett förbättrat arbetsflöde.
type: docs
weight: 100
url: /sv/net/aspose.words.drawing/textbox/previous/
---
## TextBox.Previous property

Returnerar en[`TextBox`](../) som representerar det föregående[`TextBox`](../) en sekvens av former.

```csharp
public TextBox Previous { get; }
```

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

// Endast en tom textruta får innehålla en länk.
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
