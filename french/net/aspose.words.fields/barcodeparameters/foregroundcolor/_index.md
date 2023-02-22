---
title: BarcodeParameters.ForegroundColor
second_title: Référence de l'API Aspose.Words pour .NET
description: BarcodeParameters propriété. Couleur de premier plan du code à barres 0x000000  0xFFFFFF
type: docs
weight: 110
url: /fr/net/aspose.words.fields/barcodeparameters/foregroundcolor/
---
## BarcodeParameters.ForegroundColor property

Couleur de premier plan du code à barres (0x000000 - 0xFFFFFF)

```csharp
public string ForegroundColor { get; set; }
```

### Exemples

Montre comment utiliser un générateur de code-barres.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nous pouvons utiliser une implémentation IBarcodeGenerator personnalisée pour générer des codes-barres,
// puis insérez-les dans le document en tant qu'images.
doc.FieldOptions.BarcodeGenerator = new CustomBarcodeGenerator();

// Vous trouverez ci-dessous quatre exemples de différents types de codes-barres que nous pouvons créer à l'aide de notre générateur.
// Pour chaque code-barres, nous spécifions un nouvel ensemble de paramètres de code-barres, puis générons l'image.
// Ensuite, nous pouvons insérer l'image dans le document ou l'enregistrer dans le système de fichiers local.
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
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.QR.jpg");

builder.InsertImage(img);

// 2 - Code barre EAN13 :
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "EAN13",
    BarcodeValue = "501234567890",
    DisplayText = true,
    PosCodeStyle = "CASE",
    FixCheckDigit = true
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.EAN13.jpg");
builder.InsertImage(img);

// 3 - Code barre CODE39 :
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "CODE39",
    BarcodeValue = "12345ABCDE",
    AddStartStopChar = true
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.CODE39.jpg");
builder.InsertImage(img);

// 4 - Code barre ITF14 :
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "ITF14",
    BarcodeValue = "09312345678907",
    CaseCodeStyle = "STD"
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.ITF14.jpg");
builder.InsertImage(img);

doc.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.docx");
```

### Voir également

* class [BarcodeParameters](../)
* espace de noms [Aspose.Words.Fields](../../barcodeparameters/)
* Assemblée [Aspose.Words](../../../)


