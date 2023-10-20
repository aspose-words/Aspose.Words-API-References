---
title: Comment.RemoveReply
linktitle: RemoveReply
articleTitle: RemoveReply
second_title: Aspose.Words pour .NET
description: Comment RemoveReply méthode. Supprime la réponse spécifiée à ce commentaire en C#.
type: docs
weight: 140
url: /fr/net/aspose.words/comment/removereply/
---
## Comment.RemoveReply method

Supprime la réponse spécifiée à ce commentaire.

```csharp
public void RemoveReply(Comment reply)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| reply | Comment | Le nœud de commentaire de la réponse de suppression. |

## Remarques

Tous les nœuds constitutifs de la réponse seront supprimés du document.

## Exemples

Montre comment supprimer les réponses aux commentaires.

```csharp
Document doc = new Document();

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "Another reply");

Assert.AreEqual(2, comment.Replies.Count()); 

// Vous trouverez ci-dessous deux manières de supprimer les réponses d'un commentaire.
// 1 - Utilisez la méthode "RemoveReply" pour supprimer individuellement les réponses d'un commentaire :
comment.RemoveReply(comment.Replies[0]);

Assert.AreEqual(1, comment.Replies.Count());

// 2 - Utilisez la méthode "RemoveAllReplies" pour supprimer toutes les réponses d'un commentaire d'un coup :
comment.RemoveAllReplies();

Assert.AreEqual(0, comment.Replies.Count());
```

### Voir également

* class [Comment](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
