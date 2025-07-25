---
title: TextBox.IsValidLinkTarget
linktitle: IsValidLinkTarget
articleTitle: IsValidLinkTarget
second_title: Aspose.Words for .NET
description: Discover if your TextBox can link to a target with the IsValidLinkTarget method. Enhance your UI functionality effortlessly!
type: docs
weight: 140
url: /net/aspose.words.drawing/textbox/isvalidlinktarget/
---
## TextBox.IsValidLinkTarget method

Determines whether this [`TextBox`](../) can be linked to the target [`TextBox`](../).

```csharp
public bool IsValidLinkTarget(TextBox target)
```

## Examples

Shows how to link text boxes.

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

// Create links between some of the text boxes.
if (textBox1.IsValidLinkTarget(textBox2))
    textBox1.Next = textBox2;

if (textBox2.IsValidLinkTarget(textBox3))
    textBox2.Next = textBox3;

// Only an empty text box may have a link.
Assert.That(textBox3.IsValidLinkTarget(textBox4), Is.True);

builder.MoveTo(textBoxShape4.LastParagraph);
builder.Write("Hello world!");

Assert.That(textBox3.IsValidLinkTarget(textBox4), Is.False);

if (textBox1.Next != null && textBox1.Previous == null)
    Console.WriteLine("This TextBox is the head of the sequence");

if (textBox2.Next != null && textBox2.Previous != null)
    Console.WriteLine("This TextBox is the middle of the sequence");

if (textBox3.Next == null && textBox3.Previous != null)
{
    Console.WriteLine("This TextBox is the tail of the sequence");

    // Break the forward link between textBox2 and textBox3, and then verify that they are no longer linked.
    textBox3.Previous.BreakForwardLink();
    Assert.That(textBox2.Next == null, Is.True);
    Assert.That(textBox3.Previous == null, Is.True);
}

doc.Save(ArtifactsDir + "Shape.CreateLinkBetweenTextBoxes.docx");
```

### See Also

* class [TextBox](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
