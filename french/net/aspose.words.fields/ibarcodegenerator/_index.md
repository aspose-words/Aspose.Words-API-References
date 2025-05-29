---
title: IBarcodeGenerator Interface
linktitle: IBarcodeGenerator
articleTitle: IBarcodeGenerator
second_title: Aspose.Words pour .NET
description: Découvrez l'interface Aspose.Words.Fields.IBarcodeGenerator pour la génération de codes-barres personnalisés. Dynamisez vos projets grâce à des implémentations personnalisées et optimisez les fonctionnalités !
type: docs
weight: 3070
url: /fr/net/aspose.words.fields/ibarcodegenerator/
---
## IBarcodeGenerator interface

Interface publique pour le générateur de codes-barres personnalisé. L'implémentation doit être fournie par l'utilisateur.

```csharp
public interface IBarcodeGenerator
```

## Méthodes

| Nom | La description |
| --- | --- |
| [GetBarcodeImage](../../aspose.words.fields/ibarcodegenerator/getbarcodeimage/)(*[BarcodeParameters](../barcodeparameters/)*) | Générer une image de code-barres à l'aide de l'ensemble de paramètres (pour le champ DisplayBarcode). |
| [GetOldBarcodeImage](../../aspose.words.fields/ibarcodegenerator/getoldbarcodeimage/)(*[BarcodeParameters](../barcodeparameters/)*) | Générer une image de code-barres à l'aide de l'ensemble de paramètres (pour le champ de code-barres à l'ancienne). |

## Remarques

L'instance du générateur doit être transmise via le[`BarcodeGenerator`](../fieldoptions/barcodegenerator/) propriété.

## Exemples

Montre comment utiliser un générateur de codes-barres.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Nous pouvons utiliser une implémentation IBarcodeGenerator personnalisée pour générer des codes-barres,
// puis insérez-les dans le document sous forme d'images.
doc.FieldOptions.BarcodeGenerator = new CustomBarcodeGenerator();

// Vous trouverez ci-dessous quatre exemples de différents types de codes-barres que nous pouvons créer à l'aide de notre générateur.
// Pour chaque code-barres, nous spécifions un nouvel ensemble de paramètres de code-barres, puis générons l'image.
// Ensuite, nous pouvons insérer l'image dans le document ou l'enregistrer sur le système de fichiers local.
// 1 - Code QR :
BarcodeParameters barcodeParameters = new BarcodeParameters
{
    BarcodeType = "QR",
    BarcodeValue = "ABC123",
    BackgroundColor = "0xF8BD69",
    ForegroundColor = "0xB5413B",
    ErrorCorrectionLevel = "3",
    ScalingFactor = "250",
    SymbolHeight = "1000",
    SymbolRotation = "0"
};

Image img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
#if NET461_OR_GREATER || JAVA
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.QR.jpg");
#elif NET5_0_OR_GREATER
using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "FieldOptions.BarcodeGenerator.QR.jpg"))
{
    img.Encode(fs, SKEncodedImageFormat.Jpeg, 100);
}
#endif
builder.InsertImage(img);

// 2 - Code-barres EAN13 :
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "EAN13",
    BarcodeValue = "501234567890",
    DisplayText = true,
    PosCodeStyle = "CASE",
    FixCheckDigit = true
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
#if NET461_OR_GREATER || JAVA
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.EAN13.jpg");
#elif NET5_0_OR_GREATER
using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "FieldOptions.BarcodeGenerator.EAN13.jpg"))
{
    img.Encode(fs, SKEncodedImageFormat.Jpeg, 100);
}
#endif
builder.InsertImage(img);

// 3 - Code-barres CODE39 :
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "CODE39",
    BarcodeValue = "12345ABCDE",
    AddStartStopChar = true
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
#if NET461_OR_GREATER || JAVA
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.CODE39.jpg");
#elif NET5_0_OR_GREATER
using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "FieldOptions.BarcodeGenerator.CODE39.jpg"))
{
    img.Encode(fs, SKEncodedImageFormat.Jpeg, 100);
}
#endif
builder.InsertImage(img);

// 4 - Code-barres ITF14 :
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "ITF14",
    BarcodeValue = "09312345678907",
    CaseCodeStyle = "STD"
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
#if NET461_OR_GREATER || JAVA
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.ITF14.jpg");
#elif NET5_0_OR_GREATER
using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "FieldOptions.BarcodeGenerator.ITF14.jpg"))
{
    img.Encode(fs, SKEncodedImageFormat.Jpeg, 100);
}
#endif
builder.InsertImage(img);

doc.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.docx");
```

### Voir également

* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
