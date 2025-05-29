---
title: LoadOptions.LoadFormat
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words pour .NET
description: Découvrez la propriété LoadOptions LoadFormat pour spécifier facilement les formats de documents. Optimisez le chargement avec le paramètre Auto par défaut pour des performances optimales.
type: docs
weight: 90
url: /fr/net/aspose.words.loading/loadoptions/loadformat/
---
## LoadOptions.LoadFormat property

Spécifie le format du document à charger. La valeur par défaut estAuto .

```csharp
public LoadFormat LoadFormat { get; set; }
```

## Remarques

Il est recommandé de préciser leAuto value et laissez Aspose.Words détecter automatiquement le format de fichier. Si vous connaissez le format du document que vous êtes sur le point de charger, vous pouvez spécifier explicitement le format ; cela réduira légèrement le temps de chargement en raison de la surcharge associée à la détection automatique du format. Si vous spécifiez un format de chargement explicite et qu'il s'avère erroné, la détection automatique sera invoquée et une seconde tentative de chargement du fichier sera effectuée.

## Exemples

Montre comment spécifier un URI de base lors de l'ouverture d'un document HTML.

```csharp
// Supposons que nous voulions charger un document .html contenant une image liée par un URI relatif
// tant que l'image se trouve à un autre emplacement. Dans ce cas, nous devrons convertir l'URI relative en URI absolue.
 // Nous pouvons fournir un URI de base à l'aide d'un objet HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Bien que l'image ait été cassée dans le fichier .html d'entrée, notre URI de base personnalisé nous a aidé à réparer le lien.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Ce document de sortie affichera l'image manquante.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Voir également

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
