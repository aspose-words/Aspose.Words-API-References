---
title: Class NodeCollection
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.NodeCollection klass. Representerar en samling noder av en specifik typ.
type: docs
weight: 4200
url: /sv/net/aspose.words/nodecollection/
---
## NodeCollection class

Representerar en samling noder av en specifik typ.

För att lära dig mer, besök[Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) dokumentationsartikel.

```csharp
public class NodeCollection : IEnumerable<Node>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Hämtar antalet noder i samlingen. |
| [Item](../../aspose.words/nodecollection/item/) { get; } | Hämtar en nod vid det givna indexet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | Lägger till en nod i slutet av samlingen. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Tar bort alla noder från den här samlingen och från dokumentet. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Bestämmer om en nod finns i samlingen. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Ger en enkel "foreach" stil iteration över samlingen av noder. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Returnerar det nollbaserade indexet för den angivna noden. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Infogar en nod i samlingen vid det angivna indexet. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Tar bort noden från samlingen och från dokumentet. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Tar bort noden vid det angivna indexet från samlingen och från dokumentet. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Kopierar alla noder från samlingen till en ny array av noder. |

### Anmärkningar

`NodeCollection` äger inte noderna den innehåller, snarare är det bara ett urval av nodes av den angivna typen, men noderna lagras i trädet under sina respektive överordnade noder.

`NodeCollection`stöder indexerad åtkomst, iteration och tillhandahåller metoder för att lägga till och ta bort.

De`NodeCollection` samlingen är "live", dvs. ändringar av barnen till noden object som den skapades från återspeglas omedelbart i de noder som returneras av`NodeCollection` egenskaper och metoder.

`NodeCollection` returneras av[`GetChildNodes`](../compositenode/getchildnodes/) och fungerar även som en basklass för typade nodsamlingar som t.ex[`SectionCollection`](../sectioncollection/) , [`ParagraphCollection`](../paragraphcollection/) etc.

`NodeCollection` kan vara "platt" och endast innehålla omedelbara underordnade av noden den skapades från, eller så kan den vara "djup" och innehålla alla underordnade underordnade.

### Exempel

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

### Se även

* class [Node](../node/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)


