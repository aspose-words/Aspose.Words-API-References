---
title: Node.IsComposite
linktitle: IsComposite
articleTitle: IsComposite
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Node IsComposite. Identifiez facilement si un nœud peut en contenir d'autres, améliorant ainsi la gestion et la flexibilité de votre structure de données.
type: docs
weight: 30
url: /fr/net/aspose.words/node/iscomposite/
---
## Node.IsComposite property

Retours`vrai` si ce nœud peut contenir d'autres nœuds.

```csharp
public virtual bool IsComposite { get; }
```

### Valeur de la propriété

Cette méthode renvoie`FAUX` comme[`Node`](../) ne peut pas avoir de nœuds enfants.

## Exemples

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
