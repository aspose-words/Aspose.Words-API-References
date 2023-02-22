---
title: CompositeNode.InsertAfter
second_title: Référence de l'API Aspose.Words pour .NET
description: CompositeNode méthode. Insère le nœud spécifié immédiatement après le nœud de référence spécifié.
type: docs
weight: 140
url: /fr/net/aspose.words/compositenode/insertafter/
---
## CompositeNode.InsertAfter method

Insère le nœud spécifié immédiatement après le nœud de référence spécifié.

```csharp
public Node InsertAfter(Node newChild, Node refChild)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| newChild | Node | Le nœud à insérer. |
| refChild | Node | Le nœud qui est le nœud de référence. Le newNode est placé après le refNode. |

### Return_Value

Le nœud inséré.

### Remarques

Si refChild est null, insère newChild au début de la liste des nœuds enfants.

Si le newChild est déjà dans l'arborescence, il est d'abord supprimé.

Si le nœud inséré a été créé à partir d'un autre document, vous devez utiliser [`ImportNode`](../../documentbase/importnode/) pour importer le nœud dans le document courant. Le nœud importé peut alors être inséré dans le document courant.

### Exemples

Montre comment remplacer toutes les formes de zone de texte par des formes d'image.

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

Montre comment ajouter, mettre à jour et supprimer des nœuds enfants dans la collection d'enfants d'un CompositeNode.

```csharp
Document doc = new Document();

// Un document vide, par défaut, a un paragraphe.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Les nœuds composites tels que notre paragraphe peuvent contenir d'autres nœuds composites et en ligne comme enfants.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Crée trois nœuds d'exécution supplémentaires.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Le corps du document n'affichera pas ces passages tant que nous ne les aurons pas insérés dans un nœud composite
// qui lui-même fait partie de l'arborescence des nœuds du document, comme nous l'avons fait lors de la première exécution.
// Nous pouvons déterminer où le contenu textuel des nœuds que nous insérons
// apparaît dans le document en spécifiant un emplacement d'insertion par rapport à un autre nœud du paragraphe.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Insère la deuxième séquence dans le paragraphe devant la séquence initiale.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Insère la troisième exécution après l'exécution initiale.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Insère la première séquence au début de la collection de nœuds enfants du paragraphe.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Nous pouvons modifier le contenu de l'exécution en modifiant et en supprimant les nœuds enfants existants.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Voir également

* class [Node](../../node/)
* class [CompositeNode](../)
* espace de noms [Aspose.Words](../../compositenode/)
* Assemblée [Aspose.Words](../../../)


