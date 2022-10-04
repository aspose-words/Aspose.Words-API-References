---
title: BarcodeParameters
second_title: Référence de l'API Aspose.Words pour .NET
description: Classe de conteneur pour les paramètres de codebarres à transmettre à BarcodeGenerator.
type: docs
weight: 1320
url: /fr/net/aspose.words.fields/barcodeparameters/
---
## BarcodeParameters class

Classe de conteneur pour les paramètres de code-barres à transmettre à BarcodeGenerator.

```csharp
public class BarcodeParameters
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [BarcodeParameters](barcodeparameters/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [AddStartStopChar](../../aspose.words.fields/barcodeparameters/addstartstopchar/) { get; set; } | S'il faut ajouter des caractères Start/Stop pour les types de codes-barres NW7 et CODE39. |
| [BackgroundColor](../../aspose.words.fields/barcodeparameters/backgroundcolor/) { get; set; } | Couleur de fond du code-barres (0x000000 - 0xFFFFFF) |
| [BarcodeType](../../aspose.words.fields/barcodeparameters/barcodetype/) { get; set; } | Type de code-barres. |
| [BarcodeValue](../../aspose.words.fields/barcodeparameters/barcodevalue/) { get; set; } | Données à encoder. |
| [CaseCodeStyle](../../aspose.words.fields/barcodeparameters/casecodestyle/) { get; set; } | Style d'un code de cas pour le type de code à barres ITF14. Les valeurs valides sont [STD&#x7C;EXT&#x7C;ADD] |
| [DisplayText](../../aspose.words.fields/barcodeparameters/displaytext/) { get; set; } | Afficher ou non les données de code-barres (texte) avec l'image. |
| [ErrorCorrectionLevel](../../aspose.words.fields/barcodeparameters/errorcorrectionlevel/) { get; set; } | Niveau de correction d'erreur du QR Code. Les valeurs valides sont [0, 3]. |
| [FacingIdentificationMark](../../aspose.words.fields/barcodeparameters/facingidentificationmark/) { get; set; } | Type d'une marque d'identification de face (FIM). |
| [FixCheckDigit](../../aspose.words.fields/barcodeparameters/fixcheckdigit/) { get; set; } | S'il faut corriger le chiffre de contrôle s'il est invalide. |
| [ForegroundColor](../../aspose.words.fields/barcodeparameters/foregroundcolor/) { get; set; } | Couleur de premier plan du code à barres (0x000000 - 0xFFFFFF) |
| [IsBookmark](../../aspose.words.fields/barcodeparameters/isbookmark/) { get; set; } | Si[`PostalAddress`](./postaladdress/) est le nom d'un signet. |
| [IsUSPostalAddress](../../aspose.words.fields/barcodeparameters/isuspostaladdress/) { get; set; } | Si[`PostalAddress`](./postaladdress/) est une adresse postale américaine. |
| [PosCodeStyle](../../aspose.words.fields/barcodeparameters/poscodestyle/) { get; set; } | Style d'un code-barres Point de Vente (types de code-barres UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). Les valeurs valides (insensibles à la casse) sont [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE]. |
| [PostalAddress](../../aspose.words.fields/barcodeparameters/postaladdress/) { get; set; } | Code-barres adresse postale. |
| [ScalingFactor](../../aspose.words.fields/barcodeparameters/scalingfactor/) { get; set; } | Facteur d'échelle pour le symbole. La valeur est en points de pourcentage entiers et les valeurs valides sont [10, 1000]. |
| [SymbolHeight](../../aspose.words.fields/barcodeparameters/symbolheight/) { get; set; } | Hauteur de l'image du code à barres (en twips - 1/1440 pouces) |
| [SymbolRotation](../../aspose.words.fields/barcodeparameters/symbolrotation/) { get; set; } | Rotation du symbole du code-barres. Les valeurs valides sont [0, 3]. |

### Remarques

L'ensemble des paramètres est fonction des options du champ DISPLAYBARCODE. Voir la liste exacte sur[https://msdn.microsoft.com/en-us/library/hh745901(v=office.12).aspx](https://msdn.microsoft.com/en-us/library/hh745901(v=office.12).aspx)

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

* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
