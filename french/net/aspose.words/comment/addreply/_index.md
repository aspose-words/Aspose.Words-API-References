---
title: Comment.AddReply
linktitle: AddReply
articleTitle: AddReply
second_title: Aspose.Words pour .NET
description: Améliorez vos discussions avec la méthode Comment AddReply  ajoutez facilement des réponses aux commentaires et améliorez l'engagement sur votre plateforme !
type: docs
weight: 160
url: /fr/net/aspose.words/comment/addreply/
---
## Comment.AddReply method

Ajoute une réponse à ce commentaire.

```csharp
public Comment AddReply(string author, string initial, DateTime dateTime, string text)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| author | String | Le nom de l'auteur de la réponse. |
| initial | String | L'auteur paraphe la réponse. |
| dateTime | DateTime | La date et l'heure de la réponse. |
| text | String | Le texte de réponse. |

### Return_Value

Le créé[`Comment`](../) nœud pour la réponse.

### Exceptions

| exception | condition |
| --- | --- |
| InvalidOperationException | Lève une exception si cette méthode est appelée sur le commentaire de réponse existant. |

## Remarques

En raison des limitations existantes de MS Office, un seul niveau de réponses est autorisé dans le document.

## Exemples

Montre comment ajouter un commentaire à un document, puis y répondre.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Placez le commentaire sur un nœud dans le corps du document.
// Ce commentaire apparaîtra à l'emplacement de son paragraphe,
// en dehors de la marge droite de la page, et avec une ligne pointillée le reliant à son paragraphe.
builder.CurrentParagraph.AppendChild(comment);

// Ajoutez une réponse, qui apparaîtra sous son commentaire parent.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Les commentaires et les réponses sont tous deux des nœuds de commentaire.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Les commentaires qui ne répondent pas aux autres commentaires sont de « niveau supérieur ». Ils n'ont pas de commentaires ancêtres.
Assert.Null(comment.Ancestor);

// Les réponses ont un commentaire de niveau supérieur ancêtre.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Voir également

* class [Comment](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
