---
title: Node.NextSibling
linktitle: NextSibling
articleTitle: NextSibling
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Node NextSibling pour accéder facilement au nœud suivant de votre DOM. Améliorez vos compétences JavaScript et optimisez votre codage dès aujourd'hui !
type: docs
weight: 40
url: /fr/net/aspose.words/node/nextsibling/
---
## Node.NextSibling property

Obtient le nœud suivant immédiatement ce nœud.

```csharp
public Node NextSibling { get; }
```

## Remarques

S'il n'y a pas de nœud suivant, un`nul` est renvoyé.

## Exemples

Montre comment utiliser la propriété NextSibling d'un nœud pour énumérer ses enfants immédiats.

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

Montre comment parcourir l'arbre des nœuds enfants d'un nœud composite.

```csharp
public void RecurseChildren()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // Tout nœud pouvant contenir des nœuds enfants, comme le document lui-même, est composite.
    Assert.True(doc.IsComposite);

    // Invoquez la fonction récursive qui parcourra et imprimera tous les nœuds enfants d'un nœud composite.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// Parcourt récursivement une arborescence de nœuds tout en imprimant le type de chaque nœud
/// avec un retrait dépendant de la profondeur ainsi que du contenu de tous les nœuds en ligne.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // Effectuer une récursion dans le nœud s'il s'agit d'un nœud composite. Sinon, afficher son contenu s'il s'agit d'un nœud en ligne.
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

* class [Node](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
