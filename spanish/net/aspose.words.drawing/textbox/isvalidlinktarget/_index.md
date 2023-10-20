---
title: TextBox.IsValidLinkTarget
linktitle: IsValidLinkTarget
articleTitle: IsValidLinkTarget
second_title: Aspose.Words para .NET
description: TextBox IsValidLinkTarget método. Determina si estoTextBox se puede vincular al objetivoTextBox  en C#.
type: docs
weight: 140
url: /es/net/aspose.words.drawing/textbox/isvalidlinktarget/
---
## TextBox.IsValidLinkTarget method

Determina si esto[`TextBox`](../) se puede vincular al objetivo[`TextBox`](../) .

```csharp
public bool IsValidLinkTarget(TextBox target)
```

## Ejemplos

Muestra cómo vincular cuadros de texto.

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

// Crea enlaces entre algunos de los cuadros de texto.
if (textBox1.IsValidLinkTarget(textBox2))
    textBox1.Next = textBox2;

if (textBox2.IsValidLinkTarget(textBox3))
    textBox2.Next = textBox3;

// Sólo un cuadro de texto vacío puede tener un enlace.
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

    // Rompe el vínculo de reenvío entre textBox2 y textBox3 y luego verifica que ya no estén vinculados.
    textBox3.Previous.BreakForwardLink();

    Assert.IsTrue(textBox2.Next == null);
    Assert.IsTrue(textBox3.Previous == null);
}

doc.Save(ArtifactsDir + "Shape.CreateLinkBetweenTextBoxes.docx");
```

### Ver también

* class [TextBox](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
