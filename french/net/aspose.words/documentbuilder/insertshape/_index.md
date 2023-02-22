---
title: DocumentBuilder.InsertShape
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentBuilder méthode. Insère une forme en ligne avec le type et la taille spécifiés.
type: docs
weight: 410
url: /fr/net/aspose.words/documentbuilder/insertshape/
---
## InsertShape(ShapeType, double, double) {#insertshape_1}

Insère une forme en ligne avec le type et la taille spécifiés.

```csharp
public Shape InsertShape(ShapeType shapeType, double width, double height)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| shapeType | ShapeType | Le type de forme à insérer dans le document. |
| width | Double | La largeur de la forme en points. |
| height | Double | La hauteur de la forme en points. |

### Return_Value

Le nœud de forme qui a été inséré.

### Exemples

Montre comment insérer des formes DML dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux types d'habillage que les formes peuvent avoir.
// 1 - Flottant :
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100, 
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - En ligne :
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Si vous avez besoin de créer des formes "non primitives", telles que SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded ou DiagonalCornersRounded,
// puis enregistrez le document avec la conformité "Strict" ou "Transitional", ce qui permet d'enregistrer la forme au format DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)

---

## InsertShape(ShapeType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertshape}

Insère une forme flottante avec une position, une taille et un type d'habillage de texte spécifiés.

```csharp
public Shape InsertShape(ShapeType shapeType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| shapeType | ShapeType | Le type de forme à insérer dans le document |
| horzPos | RelativeHorizontalPosition | Spécifie l'endroit à partir duquel la distance horizontale à la forme est mesurée. |
| left | Double | Distance en points entre l'origine et le côté gauche de la forme. |
| vertPos | RelativeVerticalPosition | Spécifie l'endroit à partir duquel la distance verticale à la forme est mesurée. |
| top | Double | Distance en points entre l'origine et le côté supérieur de la forme. |
| width | Double | La largeur de la forme en points. |
| height | Double | La largeur de la forme en points. |
| wrapType | WrapType | Spécifie comment habiller le texte autour de la forme. |

### Return_Value

Le nœud de forme qui a été inséré.

### Exemples

Montre comment insérer des formes DML dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux types d'habillage que les formes peuvent avoir.
// 1 - Flottant :
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100, 
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - En ligne :
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Si vous avez besoin de créer des formes "non primitives", telles que SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded ou DiagonalCornersRounded,
// puis enregistrez le document avec la conformité "Strict" ou "Transitional", ce qui permet d'enregistrer la forme au format DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)


