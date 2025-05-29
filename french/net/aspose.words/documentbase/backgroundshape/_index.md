---
title: DocumentBase.BackgroundShape
linktitle: BackgroundShape
articleTitle: BackgroundShape
second_title: Aspose.Words pour .NET
description: Découvrez la propriété BackgroundShape de DocumentBase : personnalisez facilement la forme d'arrière-plan de votre document pour un rendu visuel optimal. Optimisez votre potentiel créatif !
type: docs
weight: 10
url: /fr/net/aspose.words/documentbase/backgroundshape/
---
## DocumentBase.BackgroundShape property

Obtient ou définit la forme d'arrière-plan du document. Peut être`nul` .

```csharp
public Shape BackgroundShape { get; set; }
```

## Remarques

Microsoft Word autorise uniquement une forme qui a son[`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) propriété equal àRectangle à utiliser comme forme d'arrière-plan pour un document.

Microsoft Word ne prend en charge que les propriétés de remplissage d'une forme d'arrière-plan. Toutes les autres propriétés sont ignorées.

La définition de cette propriété sur une valeur non nulle définira également le[`DisplayBackgroundShape`](../../../aspose.words.settings/viewoptions/displaybackgroundshape/) à`vrai`.

## Exemples

Montre comment définir une forme d'arrière-plan pour chaque page d'un document.

```csharp
Document doc = new Document();

Assert.IsNull(doc.BackgroundShape);

// Le seul type de forme que nous pouvons utiliser comme arrière-plan est un rectangle.
Shape shapeRectangle = new Shape(doc, ShapeType.Rectangle);

// Il existe deux façons d'utiliser cette forme comme arrière-plan de page.
// 1 - Une couleur plate :
shapeRectangle.FillColor = System.Drawing.Color.LightBlue;
doc.BackgroundShape = shapeRectangle;

doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.FlatColor.docx");

// 2 - Une image :
shapeRectangle = new Shape(doc, ShapeType.Rectangle);
shapeRectangle.ImageData.SetImage(ImageDir + "Transparent background logo.png");

// Ajustez l'apparence de l'image pour la rendre plus adaptée comme filigrane.
shapeRectangle.ImageData.Contrast = 0.2;
shapeRectangle.ImageData.Brightness = 0.7;

doc.BackgroundShape = shapeRectangle;

Assert.IsTrue(doc.BackgroundShape.HasImage);

Aspose.Words.Saving.PdfSaveOptions saveOptions = new Aspose.Words.Saving.PdfSaveOptions
{
    CacheBackgroundGraphics = false
};

// Microsoft Word ne prend pas en charge les formes avec des images en arrière-plan,
// mais nous pouvons toujours voir ces arrière-plans dans d'autres formats de sauvegarde tels que .pdf.
doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.Image.pdf", saveOptions);
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBase](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
