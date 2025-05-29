---
title: Comment.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words pour .NET
description: Découvrez la méthode SetText, un outil convivial qui simplifie l'ajout de commentaires, améliore votre flux de travail et augmente votre productivité sans effort.
type: docs
weight: 190
url: /fr/net/aspose.words/comment/settext/
---
## Comment.SetText method

Il s'agit d'une méthode pratique qui permet de définir facilement le texte du commentaire.

```csharp
public void SetText(string text)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| text | String | Le nouveau texte du commentaire. |

## Remarques

Cette méthode permet de définir rapidement le texte d'un commentaire à partir d'une chaîne. La chaîne peut contenir des sauts de paragraphe, ce qui créera des paragraphes de texte dans le commentaire. Si vous souhaitez insérer des éléments plus complexes dans le commentaire, par exemple des signets ou des tableaux, ou appliquer une mise en forme enrichie, vous devez utiliser les classes de nœuds appropriées pour créer le texte du commentaire.

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
