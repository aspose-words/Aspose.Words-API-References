---
title: Comment.RemoveAllReplies
linktitle: RemoveAllReplies
articleTitle: RemoveAllReplies
second_title: Aspose.Words pour .NET
description: Effacez sans effort toutes les réponses à votre commentaire avec la méthode RemoveAllReplies, garantissant une discussion sans encombrement et une expérience utilisateur améliorée.
type: docs
weight: 170
url: /fr/net/aspose.words/comment/removeallreplies/
---
## Comment.RemoveAllReplies method

Supprime toutes les réponses à ce commentaire.

```csharp
public void RemoveAllReplies()
```

## Remarques

Tous les nœuds constitutifs des réponses seront supprimés du document.

## Exemples

Montre comment supprimer les réponses aux commentaires.

```csharp
Document doc = new Document();

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "Another reply");

Assert.AreEqual(2, comment.Replies.Count); 

// Vous trouverez ci-dessous deux manières de supprimer les réponses d'un commentaire.
// 1 - Utilisez la méthode « RemoveReply » pour supprimer individuellement les réponses d'un commentaire :
comment.RemoveReply(comment.Replies[0]);

Assert.AreEqual(1, comment.Replies.Count);

// 2 - Utilisez la méthode « RemoveAllReplies » pour supprimer toutes les réponses d'un commentaire à la fois :
comment.RemoveAllReplies();

Assert.AreEqual(0, comment.Replies.Count);
```

### Voir également

* class [Comment](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
