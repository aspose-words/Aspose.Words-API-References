---
title: DocumentBuilder.InsertShape
linktitle: InsertShape
articleTitle: InsertShape
second_title: Aspose.Words pour .NET
description: Ajoutez facilement des formes personnalisées en ligne grâce à la méthode InsertShape de DocumentBuilder. Améliorez vos documents avec des visuels sur mesure pour des présentations percutantes !
type: docs
weight: 460
url: /fr/net/aspose.words/documentbuilder/insertshape/
---
## InsertShape(*[ShapeType](../../../aspose.words.drawing/shapetype/), double, double*) {#insertshape_1}

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

## Exemples

Montre comment insérer des formes DML dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux types d'emballage que les formes peuvent avoir.
// 1 - Flottant :
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - En ligne :
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Si vous devez créer des formes « non primitives », telles que SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// Coins supérieurs un arrondi un coupé, Coin unique arrondi, Coins supérieurs arrondis ou Coins diagonaux arrondis,
// puis enregistrez le document avec une conformité « Stricte » ou « Transitionnelle », ce qui permet d'enregistrer la forme au format DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## InsertShape(*[ShapeType](../../../aspose.words.drawing/shapetype/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertshape}

Insère une forme flottante avec une position, une taille et un type d'habillage de texte spécifiés.

```csharp
public Shape InsertShape(ShapeType shapeType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| shapeType | ShapeType | Le type de forme à insérer dans le document |
| horzPos | RelativeHorizontalPosition | Spécifie l'endroit à partir duquel la distance horizontale par rapport à la forme est mesurée. |
| left | Double | Distance en points de l'origine au côté gauche de la forme. |
| vertPos | RelativeVerticalPosition | Spécifie l'endroit à partir duquel la distance verticale par rapport à la forme est mesurée. |
| top | Double | Distance en points de l'origine au côté supérieur de la forme. |
| width | Double | La largeur de la forme en points. |
| height | Double | La hauteur de la forme en points. |
| wrapType | WrapType | Spécifie comment envelopper le texte autour de la forme. |

### Return_Value

Le nœud de forme qui a été inséré.

## Exemples

Montre comment insérer des formes DML dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux types d'emballage que les formes peuvent avoir.
// 1 - Flottant :
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - En ligne :
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Si vous devez créer des formes « non primitives », telles que SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// Coins supérieurs un arrondi un coupé, Coin unique arrondi, Coins supérieurs arrondis ou Coins diagonaux arrondis,
// puis enregistrez le document avec une conformité « Stricte » ou « Transitionnelle », ce qui permet d'enregistrer la forme au format DML.
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
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
