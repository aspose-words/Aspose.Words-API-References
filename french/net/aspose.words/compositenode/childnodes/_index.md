---
title: CompositeNode.ChildNodes
second_title: Référence de l'API Aspose.Words pour .NET
description: CompositeNode propriété. Obtient tous les nœuds enfants immédiats de ce nœud.
type: docs
weight: 10
url: /fr/net/aspose.words/compositenode/childnodes/
---
## CompositeNode.ChildNodes property

Obtient tous les nœuds enfants immédiats de ce nœud.

```csharp
public NodeCollection ChildNodes { get; }
```

### Remarques

Noter,`ChildNodes` équivaut à appeler`GetChildNodes(NodeType.Any, false)` et crée et renvoie une nouvelle collection à chaque accès.

S'il n'y a pas de nœuds enfants, cette propriété renvoie une collection vide.

### Exemples

Montre comment parcourir la collection de nœuds enfants d'un nœud composite.

```csharp
Document doc = new Document();

// Ajoutez deux passages et une forme en tant que nœuds enfants au premier paragraphe de ce document.
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

// Parcourt la collection d'enfants immédiats du paragraphe,
// et imprimez toutes les pistes ou formes que nous trouvons à l'intérieur.
NodeCollection children = paragraph.ChildNodes;

Assert.AreEqual(3, paragraph.ChildNodes.Count);

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
    }
```

### Voir également

* class [NodeCollection](../../nodecollection/)
* class [CompositeNode](../)
* espace de noms [Aspose.Words](../../compositenode/)
* Assemblée [Aspose.Words](../../../)


