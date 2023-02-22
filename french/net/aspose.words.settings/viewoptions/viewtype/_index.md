---
title: ViewOptions.ViewType
second_title: Référence de l'API Aspose.Words pour .NET
description: ViewOptions propriété. Contrôle le mode daffichage dans Microsoft Word.
type: docs
weight: 40
url: /fr/net/aspose.words.settings/viewoptions/viewtype/
---
## ViewOptions.ViewType property

Contrôle le mode d'affichage dans Microsoft Word.

```csharp
public ViewType ViewType { get; set; }
```

### Remarques

Bien qu'Aspose.Words soit capable de lire et d'écrire cette option, son utilisation est spécifique à l'application. Par exemple MS Word 2013 ne respecte pas la valeur de cette option.

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

### Voir également

* enum [ViewType](../../viewtype/)
* class [ViewOptions](../)
* espace de noms [Aspose.Words.Settings](../../viewoptions/)
* Assemblée [Aspose.Words](../../../)


