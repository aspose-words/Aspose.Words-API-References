---
title: CompositeNode.InsertAfter
linktitle: InsertAfter
articleTitle: InsertAfter
second_title: Aspose.Words för .NET
description: Infoga enkelt noder med CompositeNode InsertAfter-metoden, vilket förbättrar din datastrukturhantering och säkerställer effektiv nodplacering.
type: docs
weight: 150
url: /sv/net/aspose.words/compositenode/insertafter/
---
## CompositeNode.InsertAfter&lt;T&gt; method

Infogar den angivna noden omedelbart efter den angivna referensnoden.

```csharp
public T InsertAfter<T>(T newChild, Node refChild)
    where T : Node
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| newChild | T | De[`Node`](../../node/) att infoga. |
| refChild | Node | De[`Node`](../../node/) det är referensnoden. Den*newChild* placeras efter*refChild*. |

### Returvärde

Den infogade noden.

## Anmärkningar

Om*refChild* är`null` , insatser*newChild* i början av listan över underordnade noder.

Om*newChild* redan finns i trädet, tas det först bort.

Om noden som infogas skapades från ett annat dokument bör du använda [`ImportNode`](../../documentbase/importnode/) för att importera noden till det aktuella dokumentet. Den importerade noden kan sedan infogas i det aktuella dokumentet.

## Exempel

Visar hur man ersätter alla textruteformer med bildformer.

```csharp
Document doc = new Document(MyDir + "Textboxes in drawing canvas.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(3, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(1, shapes.Count(s => s.ShapeType == ShapeType.Image));

foreach (Shape shape in shapes)
{
    if (shape.ShapeType == ShapeType.TextBox)
    {
        Shape replacementShape = new Shape(doc, ShapeType.Image);
        replacementShape.ImageData.SetImage(ImageDir + "Logo.jpg");
        replacementShape.Left = shape.Left;
        replacementShape.Top = shape.Top;
        replacementShape.Width = shape.Width;
        replacementShape.Height = shape.Height;
        replacementShape.RelativeHorizontalPosition = shape.RelativeHorizontalPosition;
        replacementShape.RelativeVerticalPosition = shape.RelativeVerticalPosition;
        replacementShape.HorizontalAlignment = shape.HorizontalAlignment;
        replacementShape.VerticalAlignment = shape.VerticalAlignment;
        replacementShape.WrapType = shape.WrapType;
        replacementShape.WrapSide = shape.WrapSide;

        shape.ParentNode.InsertAfter(replacementShape, shape);
        shape.Remove();
    }
}

shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(0, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(4, shapes.Count(s => s.ShapeType == ShapeType.Image));

doc.Save(ArtifactsDir + "Shape.ReplaceTextboxesWithImages.docx");
```

Visar hur man lägger till, uppdaterar och tar bort underordnade noder i en CompositeNodes samling av underordnade noder.

```csharp
Document doc = new Document();

// Ett tomt dokument har som standard ett stycke.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Sammansatta noder som vårt stycke kan innehålla andra sammansatta och inline-noder som underordnade.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Skapa ytterligare tre körnoder.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Dokumentets innehåll kommer inte att visa dessa körningar förrän vi infogar dem i en sammansatt nod
// som i sig är en del av dokumentets nodträd, precis som vi gjorde med den första körningen.
// Vi kan avgöra var textinnehållet i noder som vi infogar ska
// visas i dokumentet genom att ange en insättningsplats i förhållande till en annan nod i stycket.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Infoga den andra satsen i stycket före den första satsen.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Infoga den tredje körningen efter den första körningen.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Infoga den första körningen i början av styckets samling av underordnade noder.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Vi kan ändra innehållet i körningen genom att redigera och ta bort befintliga undernoder.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Se även

* class [Node](../../node/)
* class [CompositeNode](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
