---
title: Enum CommentDisplayMode
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Layout.CommentDisplayMode énumération. Spécifie le mode de rendu des commentaires de document.
type: docs
weight: 3090
url: /fr/net/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enumeration

Spécifie le mode de rendu des commentaires de document.

```csharp
public enum CommentDisplayMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Hide | `0` | Aucun commentaire de document n'est affiché. |
| ShowInBalloons | `1` | Rend les commentaires du document dans des bulles dans la marge. Il s'agit de la valeur par défaut. |
| ShowInAnnotations | `2` | Rend les commentaires du document dans les annotations. Ceci est uniquement disponible pour le format Pdf. |

### Exemples

Montre comment afficher les commentaires lors de l'enregistrement d'un document dans un format rendu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");
builder.CurrentParagraph.AppendChild(comment);

// ShowInAnnotations n'est disponible qu'aux formats Pdf1.7 et Pdf1.5.
// Dans d'autres formats, cela fonctionnera de la même manière que Hide.
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


