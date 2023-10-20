---
title: Node.CustomNodeId
linktitle: CustomNodeId
articleTitle: CustomNodeId
second_title: Aspose.Words pour .NET
description: Node CustomNodeId propriété. Spécifie lidentifiant de nœud personnalisé en C#.
type: docs
weight: 10
url: /fr/net/aspose.words/node/customnodeid/
---
## Node.CustomNodeId property

Spécifie l'identifiant de nœud personnalisé.

```csharp
public int CustomNodeId { get; set; }
```

## Remarques

La valeur par défaut est zéro.

Cet identifiant peut être défini et utilisé arbitrairement. Par exemple, comme clé pour obtenir des données externes.

Remarque importante : la valeur spécifiée n'est pas enregistrée dans un fichier de sortie et n'existe que pendant la durée de vie du nœud.

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

* class [Node](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
