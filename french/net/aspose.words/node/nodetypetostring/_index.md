---
title: Node.NodeTypeToString
linktitle: NodeTypeToString
articleTitle: NodeTypeToString
second_title: Aspose.Words pour .NET
description: Node NodeTypeToString méthode. Une méthode utilitaire qui convertit une valeur dénumération de type de nœud en une chaîne conviviale en C#.
type: docs
weight: 170
url: /fr/net/aspose.words/node/nodetypetostring/
---
## Node.NodeTypeToString method

Une méthode utilitaire qui convertit une valeur d'énumération de type de nœud en une chaîne conviviale.

```csharp
public static string NodeTypeToString(NodeType nodeType)
```

## Exemples

Montre comment utiliser la propriété NextSibling d’un nœud pour énumérer ses enfants immédiats.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

for (Node node = doc.FirstSection.Body.FirstChild; node != null; node = node.NextSibling)
{
    Console.WriteLine();
    Console.WriteLine($"Node type: {Node.NodeTypeToString(node.NodeType)}");

    string contents = node.GetText().Trim();
    Console.WriteLine(contents == string.Empty ? "This node contains no text" : $"Contents: \"{node.GetText().Trim()}\"");
}
```

Montre comment parcourir l’arborescence des nœuds enfants d’un nœud composite.

```csharp
public void RecurseChildren()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // Tout nœud pouvant contenir des nœuds enfants, comme le document lui-même, est composite.
    Assert.True(doc.IsComposite);

    // Invoque la fonction récursive qui parcourra et imprimera tous les nœuds enfants d'un nœud composite.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// Parcourt récursivement une arborescence de nœuds tout en imprimant le type de chaque nœud
/// avec un retrait en fonction de la profondeur ainsi que du contenu de tous les nœuds en ligne.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // Récursion dans le nœud s'il s'agit d'un nœud composite. Sinon, imprimez son contenu s'il s'agit d'un nœud en ligne.
        if (childNode.IsComposite)
        {
            Console.WriteLine();
            TraverseAllNodes((CompositeNode)childNode, depth + 1);
        }
        else if (childNode is Inline)
        {
            Console.WriteLine($" - \"{childNode.GetText().Trim()}\"");
        }
        else
        {
            Console.WriteLine();
        }
    }
}
```

### Voir également

* enum [NodeType](../../nodetype/)
* class [Node](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
