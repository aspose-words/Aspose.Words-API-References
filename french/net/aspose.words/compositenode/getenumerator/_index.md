---
title: CompositeNode.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words pour .NET
description: CompositeNode GetEnumerator méthode. Fournit la prise en charge de chaque itération de style sur les nœuds enfants de ce nœud en C#.
type: docs
weight: 100
url: /fr/net/aspose.words/compositenode/getenumerator/
---
## CompositeNode.GetEnumerator method

Fournit la prise en charge de chaque itération de style sur les nœuds enfants de ce nœud.

```csharp
public IEnumerator<Node> GetEnumerator()
```

## Exemples

Montre comment parcourir la collection de nœuds enfants d’un nœud composite.

```csharp
Document doc = new Document();

// Ajoutez deux tracés et une forme en tant que nœuds enfants au premier paragraphe de ce document.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Notez que le 'CustomNodeId' n'est pas enregistré dans un fichier de sortie et n'existe que pendant la durée de vie du nœud.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Parcourir la collection d'enfants immédiats du paragraphe,
// et imprimons toutes les courses ou formes que nous trouvons à l'intérieur.
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, false).Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
            break;
    }
```

### Voir également

* class [Node](../../node/)
* class [CompositeNode](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
