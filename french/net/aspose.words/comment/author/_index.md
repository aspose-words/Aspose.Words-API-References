---
title: Author
second_title: Référence de l'API Aspose.Words pour .NET
description: Renvoie ou définit le nom de lauteur dun commentaire.
type: docs
weight: 30
url: /fr/net/aspose.words/comment/author/
---
## Comment.Author property

Renvoie ou définit le nom de l'auteur d'un commentaire.

```csharp
public string Author { get; set; }
```

### Remarques

Ne peut pas être nulle.

La valeur par défaut est une chaîne vide.

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

* class [Comment](../../comment)
* espace de noms [Aspose.Words](../../comment)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
