---
title: Comment.Replies
second_title: Référence de l'API Aspose.Words pour .NET
description: Comment propriété. Renvoie une collection deComment objets qui sont des enfants immédiats du commentaire spécifié.
type: docs
weight: 90
url: /fr/net/aspose.words/comment/replies/
---
## Comment.Replies property

Renvoie une collection de[`Comment`](../) objets qui sont des enfants immédiats du commentaire spécifié.

```csharp
public CommentCollection Replies { get; }
```

### Exemples

Montre comment imprimer tous les commentaires d'un document et leurs réponses.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);

// Si un commentaire n'a pas d'ancêtre, il s'agit d'un commentaire "de niveau supérieur" par opposition à un commentaire de type réponse.
// Affiche tous les commentaires de haut niveau avec toutes les réponses qu'ils peuvent avoir.
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

* class [CommentCollection](../../commentcollection/)
* class [Comment](../)
* espace de noms [Aspose.Words](../../comment/)
* Assemblée [Aspose.Words](../../../)


