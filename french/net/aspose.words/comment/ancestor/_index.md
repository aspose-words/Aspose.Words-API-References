---
title: Comment.Ancestor
linktitle: Ancestor
articleTitle: Ancestor
second_title: Aspose.Words pour .NET
description: Récupérez l'objet parent Commentaire grâce à notre propriété Ancestor. Idéal pour naviguer dans les fils de commentaires et améliorer l'engagement des utilisateurs.
type: docs
weight: 20
url: /fr/net/aspose.words/comment/ancestor/
---
## Comment.Ancestor property

Renvoie le parent[`Comment`](../)objet. Retours`nul` pour les commentaires de haut niveau.

```csharp
public Comment Ancestor { get; }
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

* class [Comment](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
