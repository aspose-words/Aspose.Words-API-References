---
title: Revision.ParentStyle
linktitle: ParentStyle
articleTitle: ParentStyle
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Revision ParentStyle, qui identifie le propriétaire immédiat du style parent pour les révisions StyleDefinitionChange. Optimisez votre processus de style !
type: docs
weight: 50
url: /fr/net/aspose.words/revision/parentstyle/
---
## Revision.ParentStyle property

Obtient le style parent immédiat (propriétaire) de cette révision. Cette propriété fonctionnera uniquement pour leStyleDefinitionChange type de révision.

```csharp
public Style ParentStyle { get; }
```

## Remarques

Si cette révision concerne des modifications sur les nœuds du document, utilisez[`ParentNode`](../parentnode/) à la place.

## Exemples

Montre comment travailler avec la collection de révisions d'un document.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");
RevisionCollection revisions = doc.Revisions;

// Cette collection elle-même possède une collection de groupes de révision.
// Chaque groupe est une séquence de révisions adjacentes.
Console.WriteLine($"{revisions.Groups.Count} revision groups:");

// Itérer sur la collection de groupes et imprimer le texte concerné par la révision.
using (IEnumerator<RevisionGroup> e = revisions.Groups.GetEnumerator())
{
    while (e.MoveNext())
    {
        Console.WriteLine($"\tGroup type \"{e.Current.RevisionType}\", " +
                          $"author: {e.Current.Author}, contents: [{e.Current.Text.Trim()}]");
    }
}

// Chaque exécution affectée par une révision obtient un objet de révision correspondant.
// La collection de révisions est considérablement plus grande que la forme condensée que nous avons imprimée ci-dessus,
// en fonction du nombre d'exécutions dans lesquelles nous avons segmenté le document lors de l'édition de Microsoft Word.
Console.WriteLine($"\n{revisions.Count} revisions:");

using (IEnumerator<Revision> e = revisions.GetEnumerator())
{
    while (e.MoveNext())
    {
        // Un StyleDefinitionChange affecte strictement les styles, et non les nœuds de document. Cela concerne le « ParentStyle ».
        // la propriété sera toujours utilisée, tandis que le ParentNode sera toujours nul.
        // Étant donné que tous les autres changements affectent les nœuds, ParentNode sera à l'inverse utilisé et ParentStyle sera nul.
        if (e.Current.RevisionType == RevisionType.StyleDefinitionChange)
        {
            Console.WriteLine($"\tRevision type \"{e.Current.RevisionType}\", " +
                              $"author: {e.Current.Author}, style: [{e.Current.ParentStyle.Name}]");
        }
        else
        {
            Console.WriteLine($"\tRevision type \"{e.Current.RevisionType}\", " +
                              $"author: {e.Current.Author}, contents: [{e.Current.ParentNode.GetText().Trim()}]");
        }
    }
}

// Rejeter toutes les révisions via la collection, rétablissant ainsi le document dans sa forme d'origine.
revisions.RejectAll();

Assert.AreEqual(0, revisions.Count);
```

### Voir également

* class [Style](../../style/)
* class [Revision](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
