---
title: Enum ViewType
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Settings.ViewType énumération. Valeurs possibles pour le mode daffichage dans Microsoft Word.
type: docs
weight: 5960
url: /fr/net/aspose.words.settings/viewtype/
---
## ViewType enumeration

Valeurs possibles pour le mode d'affichage dans Microsoft Word.

```csharp
public enum ViewType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Le document doit être rendu dans la vue par défaut de l'application. |
| Reading | `0` | Le document doit être rendu dans la vue par défaut de l'application. |
| PageLayout | `1` | Le document doit être ouvert dans une vue qui affiche le document tel qu'il sera imprimé. |
| Outline | `3` | Le document doit être rendu dans une vue optimisée pour la présentation ou la création de documents longs. |
| Normal | `4` | Le document doit être rendu dans une vue optimisée pour la présentation ou la création de documents longs. |
| Web | `5` | Le document doit être rendu dans une vue imitant la façon dont ce document serait affiché dans une page Web. |

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

* class [ViewOptions](../viewoptions/)
* property [ViewType](../viewoptions/viewtype/)
* espace de noms [Aspose.Words.Settings](../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../)


