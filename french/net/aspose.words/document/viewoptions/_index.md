---
title: Document.ViewOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Document propriété. Fournit des options pour contrôler laffichage du document dans Microsoft Word.
type: docs
weight: 450
url: /fr/net/aspose.words/document/viewoptions/
---
## Document.ViewOptions property

Fournit des options pour contrôler l'affichage du document dans Microsoft Word.

```csharp
public ViewOptions ViewOptions { get; }
```

### Exemples

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

// Définissez la propriété "ZoomType" sur "ZoomType.PageWidth" pour obtenir Microsoft Word
// pour zoomer automatiquement le document pour l'adapter à la largeur de la page.
// Définissez la propriété "ZoomType" sur "ZoomType.FullPage" pour obtenir Microsoft Word
// pour zoomer automatiquement le document afin de rendre visible toute la première page.
// Définissez la propriété "ZoomType" sur "ZoomType.TextFit" pour obtenir Microsoft Word
// pour agrandir automatiquement le document afin qu'il corresponde aux marges intérieures du texte de la première page.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### Voir également

* class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)


