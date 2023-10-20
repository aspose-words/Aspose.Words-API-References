---
title: ViewOptions.ZoomPercent
linktitle: ZoomPercent
articleTitle: ZoomPercent
second_title: Aspose.Words pour .NET
description: ViewOptions ZoomPercent propriété. Obtient ou définit le pourcentage entre 10 et 500 auquel vous souhaitez afficher votre document en C#.
type: docs
weight: 50
url: /fr/net/aspose.words.settings/viewoptions/zoompercent/
---
## ViewOptions.ZoomPercent property

Obtient ou définit le pourcentage (entre 10 et 500) auquel vous souhaitez afficher votre document.

```csharp
public int ZoomPercent { get; set; }
```

## Remarques

Si la valeur est 0, cette propriété utilise 100 à la place, sinon si la valeur est inférieure à 10 ou supérieure à 500 , cette propriété renvoie.

Bien qu'Aspose.Words soit capable de lire et d'écrire cette option, son utilisation est spécifique à l'application. Par exemple MS Word 2013 ne respecte pas la valeur de cette option.

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

### Voir également

* class [ViewOptions](../)
* espace de noms [Aspose.Words.Settings](../../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../../)
