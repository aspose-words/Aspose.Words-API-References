---
title: BarcodeParameters.AddStartStopChar
linktitle: AddStartStopChar
articleTitle: AddStartStopChar
second_title: Aspose.Words para .NET
description: BarcodeParameters AddStartStopChar propiedad. Si se deben agregar caracteres de inicio/parada para los tipos de códigos de barras NW7 y CODE39 en C#.
type: docs
weight: 20
url: /es/net/aspose.words.fields/barcodeparameters/addstartstopchar/
---
## BarcodeParameters.AddStartStopChar property

Si se deben agregar caracteres de inicio/parada para los tipos de códigos de barras NW7 y CODE39.

```csharp
public bool AddStartStopChar { get; set; }
```

## Ejemplos

Muestra cómo utilizar un generador de códigos de barras.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Podemos usar una implementación personalizada de IBarcodeGenerator para generar códigos de barras,
// y luego insertarlos en el documento como imágenes.
doc.FieldOptions.BarcodeGenerator = new CustomBarcodeGenerator();

// A continuación se muestran cuatro ejemplos de diferentes tipos de códigos de barras que podemos crear usando nuestro generador.
// Para cada código de barras, especificamos un nuevo conjunto de parámetros de código de barras y luego generamos la imagen.
// Luego, podemos insertar la imagen en el documento o guardarla en el sistema de archivos local.
// 1 - código QR:
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

// 2 - Código de barras EAN13:
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

// 3 - código de barras CODE39:
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "CODE39",
    BarcodeValue = "12345ABCDE",
    AddStartStopChar = true
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.CODE39.jpg");
builder.InsertImage(img);

// 4 - Código de barras ITF14:
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

### Ver también

* class [BarcodeParameters](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
