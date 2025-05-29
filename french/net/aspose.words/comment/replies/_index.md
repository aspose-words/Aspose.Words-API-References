---
title: Comment.Replies
linktitle: Replies
articleTitle: Replies
second_title: Aspose.Words pour .NET
description: Découvrez les réponses aux commentaires. Accédez à une collection d'objets « Commentaires » qui répondent directement à votre commentaire, améliorant ainsi l'engagement et l'interaction des utilisateurs.
type: docs
weight: 110
url: /fr/net/aspose.words/comment/replies/
---
## Comment.Replies property

Renvoie une collection de[`Comment`](../) objets qui sont des enfants immédiats du commentaire spécifié.

```csharp
public CommentCollection Replies { get; }
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

* class [CommentCollection](../../commentcollection/)
* class [Comment](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
