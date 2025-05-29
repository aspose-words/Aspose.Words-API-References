---
title: CommentDisplayMode Enum
linktitle: CommentDisplayMode
articleTitle: CommentDisplayMode
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Layout.CommentDisplayMode pour un rendu optimisé des commentaires de documents. Améliorez la clarté et la présentation de vos documents dès aujourd'hui !
type: docs
weight: 3740
url: /fr/net/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enumeration

Spécifie le mode de rendu des commentaires du document.

```csharp
public enum CommentDisplayMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Hide | `0` | Aucun commentaire de document n'est rendu. |
| ShowInBalloons | `1` | Affiche les commentaires du document dans des bulles en marge. Il s'agit de la valeur par défaut. |
| ShowInAnnotations | `2` | Affiche les commentaires du document sous forme d'annotations. Disponible uniquement pour le format PDF. |

## Exemples

Montre comment afficher les commentaires lors de l'enregistrement d'un document dans un format rendu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");
builder.CurrentParagraph.AppendChild(comment);

// ShowInAnnotations est uniquement disponible aux formats Pdf1.7 et Pdf1.5.
// Dans d'autres formats, cela fonctionnera de manière similaire à Masquer.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInAnnotations;

doc.Save(ArtifactsDir + "Document.ShowCommentsInAnnotations.pdf");

// Notez qu'il est nécessaire de reconstruire la mise en page du document (via la méthode Document.UpdatePageLayout())
// après avoir modifié les valeurs de Document.LayoutOptions.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInBalloons;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.ShowCommentsInBalloons.pdf");
```

### Voir également

* espace de noms [Aspose.Words.Layout](../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../)
