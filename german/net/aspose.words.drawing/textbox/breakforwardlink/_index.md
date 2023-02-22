---
title: TextBox.BreakForwardLink
second_title: Aspose.Words für .NET-API-Referenz
description: TextBox methode. Unterbricht den Link zur nächsten TextBox.
type: docs
weight: 120
url: /de/net/aspose.words.drawing/textbox/breakforwardlink/
---
## TextBox.BreakForwardLink method

Unterbricht den Link zur nächsten TextBox.

```csharp
public void BreakForwardLink()
```

### Bemerkungen

BreakForwardLink() unterbricht nicht alle anderen Verknüpfungen in der aktuellen Sequenz von Formen. Zum Beispiel: 1-2-3-4-Sequenz und BreakForwardLink im 2. Textfeld erstellt zwei Sequenzen 1-2, 3-4.

### Beispiele

Zeigt, wie Textfelder verknüpft werden.

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

// Verknüpfungen zwischen einigen Textfeldern erstellen.
if (textBox1.IsValidLinkTarget(textBox2))
    textBox1.Next = textBox2;

if (textBox2.IsValidLinkTarget(textBox3))
    textBox2.Next = textBox3;

// Nur ein leeres Textfeld darf einen Link haben.
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

    // Unterbrechen Sie die Vorwärtsverknüpfung zwischen textBox2 und textBox3 und überprüfen Sie dann, ob sie nicht mehr verknüpft sind.
    textBox3.Previous.BreakForwardLink();

    Assert.IsTrue(textBox2.Next == null);
    Assert.IsTrue(textBox3.Previous == null);
}

doc.Save(ArtifactsDir + "Shape.CreateLinkBetweenTextBoxes.docx");
```

### Siehe auch

* class [TextBox](../)
* namensraum [Aspose.Words.Drawing](../../textbox/)
* Montage [Aspose.Words](../../../)


