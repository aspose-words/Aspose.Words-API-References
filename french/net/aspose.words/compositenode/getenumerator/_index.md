---
title: CompositeNode.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words pour .NET
description: Découvrez la méthode CompositeNode GetEnumerator pour une itération fluide sur les nœuds enfants. Améliorez votre efficacité de codage grâce à cette puissante fonctionnalité !
type: docs
weight: 120
url: /fr/net/aspose.words/compositenode/getenumerator/
---
## CompositeNode.GetEnumerator method

Fournit un support pour chaque itération de style sur les nœuds enfants de ce nœud.

```csharp
public IEnumerator<Node> GetEnumerator()
```

## Exemples

Montre comment imprimer tous les commentaires d'un document et leurs réponses.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// Si un commentaire n'a pas d'ancêtre, il s'agit d'un commentaire de « niveau supérieur » par opposition à un commentaire de type réponse.
// Imprimez tous les commentaires de niveau supérieur ainsi que toutes les réponses qu'ils peuvent contenir.
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null).ToList())
{
    Console.WriteLine("Top-level comment:");
    Console.WriteLine($"\t\"{comment.GetText().Trim()}\", by {comment.Author}");
    Console.WriteLine($"Has {comment.Replies.Count} replies");
    foreach (Comment commentReply in comment.Replies)
    {
        Console.WriteLine($"\t\"{commentReply.GetText().Trim()}\", by {commentReply.Author}");
    }
    Console.WriteLine();
}
```

### Voir également

* class [Node](../../node/)
* class [CompositeNode](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
