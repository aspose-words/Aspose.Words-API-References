---
title: LayoutOptions.CommentDisplayMode
second_title: Référence de l'API Aspose.Words pour .NET
description: LayoutOptions propriété. Obtient ou définit la manière dont les commentaires sont rendus. La valeur par défaut estShowInBalloons .
type: docs
weight: 30
url: /fr/net/aspose.words.layout/layoutoptions/commentdisplaymode/
---
## LayoutOptions.CommentDisplayMode property

Obtient ou définit la manière dont les commentaires sont rendus. La valeur par défaut estShowInBalloons .

```csharp
public CommentDisplayMode CommentDisplayMode { get; set; }
```

### Remarques

Notez que les révisions ne sont pas affichées dans les bulles pourShowInAnnotations .

### Exemples

Montre comment afficher les commentaires lors de l'enregistrement d'un document dans un format rendu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");
builder.CurrentParagraph.AppendChild(comment);

// ShowInAnnotations est uniquement disponible aux formats Pdf1.7 et Pdf1.5.
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

* enum [CommentDisplayMode](../../commentdisplaymode/)
* class [LayoutOptions](../)
* espace de noms [Aspose.Words.Layout](../../layoutoptions/)
* Assemblée [Aspose.Words](../../../)


