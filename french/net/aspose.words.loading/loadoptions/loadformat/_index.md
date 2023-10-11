---
title: LoadOptions.LoadFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: LoadOptions propriété. Spécifie le format du document à charger. La valeur par défaut estAuto .
type: docs
weight: 90
url: /fr/net/aspose.words.loading/loadoptions/loadformat/
---
## LoadOptions.LoadFormat property

Spécifie le format du document à charger. La valeur par défaut estAuto .

```csharp
public LoadFormat LoadFormat { get; set; }
```

### Remarques

Il est recommandé de préciser leAuto valeur et laissez Aspose.Words détecter le format de fichier automatiquement. Si vous connaissez le format du document que vous êtes sur le point de charger, vous pouvez spécifier explicitement le format , ce qui réduira légèrement le temps de chargement en raison de la surcharge associée à la détection automatique du format. Si vous spécifiez un format de chargement explicite, il deviendra s'il s'avère erroné, la détection automatique sera invoquée et une seconde tentative de chargement du fichier sera effectuée.

### Exemples

Montre comment spécifier un URI de base lors de l'ouverture d'un document HTML.

```csharp
// Supposons que nous voulions charger un document .html contenant une image liée par un URI relatif
// alors que l'image se trouve à un emplacement différent. Dans ce cas, nous devrons résoudre l’URI relatif en un URI absolu.
 // Nous pouvons fournir un URI de base en utilisant un objet HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Alors que l'image était cassée dans l'entrée .html, notre URI de base personnalisé nous a aidé à réparer le lien.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Ce document de sortie affichera l'image manquante.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Voir également

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../loadoptions/)
* Assemblée [Aspose.Words](../../../)


