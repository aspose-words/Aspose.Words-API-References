---
title: Document.ViewOptions
linktitle: ViewOptions
articleTitle: ViewOptions
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Document ViewOptions pour personnaliser vos paramètres d’affichage Microsoft Word pour une expérience de visualisation sur mesure.
type: docs
weight: 490
url: /fr/net/aspose.words/document/viewoptions/
---
## Document.ViewOptions property

Fournit des options pour contrôler la façon dont le document est affiché dans Microsoft Word.

```csharp
public ViewOptions ViewOptions { get; }
```

## Exemples

Montre comment définir un facteur de zoom personnalisé, que les anciennes versions de Microsoft Word appliqueront à un document lors du chargement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.ViewOptions.ViewType = ViewType.PageLayout;
doc.ViewOptions.ZoomPercent = 50;

Assert.AreEqual(ZoomType.Custom, doc.ViewOptions.ZoomType);
Assert.AreEqual(ZoomType.None, doc.ViewOptions.ZoomType);

doc.Save(ArtifactsDir + "ViewOptions.SetZoomPercentage.doc");
```

Montre comment définir un type de zoom personnalisé, que les anciennes versions de Microsoft Word appliqueront à un document lors du chargement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Définissez la propriété « ZoomType » sur « ZoomType.PageWidth » pour obtenir Microsoft Word
// pour zoomer automatiquement le document pour l'adapter à la largeur de la page.
// Définissez la propriété « ZoomType » sur « ZoomType.FullPage » pour obtenir Microsoft Word
// pour zoomer automatiquement le document afin de rendre toute la première page visible.
// Définissez la propriété « ZoomType » sur « ZoomType.TextFit » pour obtenir Microsoft Word
// pour zoomer automatiquement le document pour l'adapter aux marges de texte intérieures de la première page.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### Voir également

* class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
