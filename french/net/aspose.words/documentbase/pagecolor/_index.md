---
title: DocumentBase.PageColor
linktitle: PageColor
articleTitle: PageColor
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PageColor de DocumentBase pour personnaliser facilement la couleur de page de votre document. Simplifiez la conception grâce à cette fonctionnalité intuitive !
type: docs
weight: 70
url: /fr/net/aspose.words/documentbase/pagecolor/
---
## DocumentBase.PageColor property

Obtient ou définit la couleur de page du document. Cette propriété est une version simplifiée de[`BackgroundShape`](../backgroundshape/) .

```csharp
public Color PageColor { get; set; }
```

## Remarques

Cette propriété fournit un moyen simple de spécifier une couleur de page unie pour le document. La définition de cette propriété crée et définit une couleur de page unie appropriée.[`BackgroundShape`](../backgroundshape/).

Si la couleur de la page n'est pas définie (par exemple, il n'y a pas de forme d'arrière-plan dans le document), renvoie Empty.

## Exemples

Montre comment définir la couleur d'arrière-plan de toutes les pages d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.PageColor = System.Drawing.Color.LightGray;

doc.Save(ArtifactsDir + "DocumentBase.SetPageColor.docx");
```

### Voir également

* class [DocumentBase](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
