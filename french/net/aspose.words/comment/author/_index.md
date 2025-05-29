---
title: Comment.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words pour .NET
description: Gérez facilement les auteurs des commentaires grâce à la propriété Auteur du commentaire. Renseignez ou définissez facilement les noms des auteurs pour améliorer l'engagement des utilisateurs et la clarté du contenu.
type: docs
weight: 30
url: /fr/net/aspose.words/comment/author/
---
## Comment.Author property

Renvoie ou définit le nom de l'auteur d'un commentaire.

```csharp
public string Author { get; set; }
```

## Remarques

Ne peut pas être`nul`.

La valeur par défaut est une chaîne vide.

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
