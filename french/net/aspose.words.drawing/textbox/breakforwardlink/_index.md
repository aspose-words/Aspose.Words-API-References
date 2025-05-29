---
title: TextBox.BreakForwardLink
linktitle: BreakForwardLink
articleTitle: BreakForwardLink
second_title: Aspose.Words pour .NET
description: Découvrez la méthode BreakForwardLink pour délier facilement vos zones de texte et améliorer l'expérience utilisateur et la navigation dans les formulaires. Optimisez votre interface utilisateur dès aujourd'hui !
type: docs
weight: 130
url: /fr/net/aspose.words.drawing/textbox/breakforwardlink/
---
## TextBox.BreakForwardLink method

Rompt le lien vers le suivant[`TextBox`](../) .

```csharp
public void BreakForwardLink()
```

## Remarques

`BreakForwardLink` ne rompt pas tous les autres liens dans la séquence actuelle de formes. Par exemple : séquence 1-2-3-4 et`BreakForwardLink` dans la 2ème zone de texte, deux séquences 1-2, 3-4 seront créées.

## Exemples

Montre comment lier des zones de texte.

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

// Créer des liens entre certaines zones de texte.
if (textBox1.IsValidLinkTarget(textBox2))
    textBox1.Next = textBox2;

if (textBox2.IsValidLinkTarget(textBox3))
    textBox2.Next = textBox3;

// Seule une zone de texte vide peut contenir un lien.
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

    // Rompre le lien direct entre textBox2 et textBox3, puis vérifier qu'ils ne sont plus liés.
    textBox3.Previous.BreakForwardLink();
    Assert.IsTrue(textBox2.Next == null);
    Assert.IsTrue(textBox3.Previous == null);
}

doc.Save(ArtifactsDir + "Shape.CreateLinkBetweenTextBoxes.docx");
```

### Voir également

* class [TextBox](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
