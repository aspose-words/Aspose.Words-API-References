---
title: Comment.AddReply
second_title: Référence de l'API Aspose.Words pour .NET
description: Comment méthode. Ajoute une réponse à ce commentaire.
type: docs
weight: 120
url: /fr/net/aspose.words/comment/addreply/
---
## Comment.AddReply method

Ajoute une réponse à ce commentaire.

```csharp
public Comment AddReply(string author, string initial, DateTime dateTime, string text)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| author | String | Nom de l'auteur de la réponse. |
| initial | String | L'auteur paraphe la réponse. |
| dateTime | DateTime | La date et l'heure de la réponse. |
| text | String | Le texte de réponse. |

### Return_Value

Le créé[`Comment`](../) nœud pour la réponse.

### Remarques

En raison des limitations existantes de MS Office, un seul niveau de réponses est autorisé dans le document. Une exception de typeInvalidOperationException sera déclenché si cette méthode est appelée sur le commentaire de réponse existant.

### Exemples

Montre comment ajouter un commentaire à un document, puis y répondre.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Place le commentaire à un nœud dans le corps du document.
// Ce commentaire apparaîtra à l'emplacement de son paragraphe,
// en dehors de la marge de droite de la page, et avec une ligne pointillée la reliant à son paragraphe.
builder.CurrentParagraph.AppendChild(comment);

// Ajouter une réponse, qui apparaîtra sous son commentaire parent.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Les commentaires et les réponses sont tous deux des nœuds de commentaire.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Les commentaires qui ne répondent pas aux autres commentaires sont "de niveau supérieur". Ils n'ont pas de commentaires d'ancêtre.
Assert.Null(comment.Ancestor);

// Les réponses ont un commentaire de niveau supérieur ancêtre.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Voir également

* class [Comment](../)
* espace de noms [Aspose.Words](../../comment/)
* Assemblée [Aspose.Words](../../../)


