---
title: Comment.Ancestor
linktitle: Ancestor
articleTitle: Ancestor
second_title: Aspose.Words pour .NET
description: Comment Ancestor propriété. Renvoie le parentComment objet. Retournul pour les commentaires de niveau supérieur en C#.
type: docs
weight: 20
url: /fr/net/aspose.words/comment/ancestor/
---
## Comment.Ancestor property

Renvoie le parent[`Comment`](../) objet. Retour`nul` pour les commentaires de niveau supérieur.

```csharp
public Comment Ancestor { get; }
```

## Exemples

Montre comment imprimer tous les commentaires d'un document et leurs réponses.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// Si un commentaire n'a pas d'ancêtre, il s'agit d'un commentaire de "niveau supérieur" par opposition à un commentaire de type réponse.
// Imprime tous les commentaires de niveau supérieur ainsi que leurs réponses éventuelles.
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null))
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

* class [Comment](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
