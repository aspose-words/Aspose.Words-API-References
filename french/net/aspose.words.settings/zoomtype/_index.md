---
title: ZoomType Enum
linktitle: ZoomType
articleTitle: ZoomType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Settings.ZoomType pour personnaliser les tailles d'affichage des documents dans Microsoft Word pour une visualisation et une productivité optimales.
type: docs
weight: 6810
url: /fr/net/aspose.words.settings/zoomtype/
---
## ZoomType enumeration

Valeurs possibles pour la taille ou la taille du document qui apparaît à l'écran dans Microsoft Word.

```csharp
public enum ZoomType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Custom | `0` | Le pourcentage de zoom est défini explicitement. Il n'est pas recalculé automatiquement lorsque la taille du contrôle change. |
| None | `0` | Indique d'utiliser le pourcentage de zoom explicite. Identique àCustom . |
| FullPage | `1` | Le pourcentage de zoom est automatiquement recalculé pour s'adapter à une page entière. |
| PageWidth | `2` | Le pourcentage de zoom est automatiquement recalculé pour s'adapter à la largeur de la page. |
| TextFit | `3` | Le pourcentage de zoom est automatiquement recalculé pour s'adapter au texte. |

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

* class [ViewOptions](../viewoptions/)
* property [ZoomType](../viewoptions/zoomtype/)
* espace de noms [Aspose.Words.Settings](../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../)
