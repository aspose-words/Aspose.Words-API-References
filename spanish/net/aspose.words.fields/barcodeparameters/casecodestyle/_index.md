---
title: BarcodeParameters.CaseCodeStyle
linktitle: CaseCodeStyle
articleTitle: CaseCodeStyle
second_title: Aspose.Words para .NET
description: Descubra la propiedad CaseCodeStyle para códigos de barras ITF14. Explore opciones válidas como STDEXTADD para mejorar el diseño y la funcionalidad de sus códigos de barras.
type: docs
weight: 60
url: /es/net/aspose.words.fields/barcodeparameters/casecodestyle/
---
## BarcodeParameters.CaseCodeStyle property

Estilo de código de caja para el código de barras ITF14. Los valores válidos son [STD&#x7C;EXT&#x7C;ADD]

```csharp
public string CaseCodeStyle { get; set; }
```

## Ejemplos

Muestra cómo utilizar un generador de código de barras.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Podemos utilizar una implementación personalizada de IBarcodeGenerator para generar códigos de barras,
// y luego insertarlos en el documento como imágenes.
doc.FieldOptions.BarcodeGenerator = new CustomBarcodeGenerator();

A continuación se muestran cuatro ejemplos de diferentes tipos de códigos de barras que podemos crear usando nuestro generador.
// Para cada código de barras, especificamos un nuevo conjunto de parámetros de código de barras y luego generamos la imagen.
//Después podemos insertar la imagen en el documento, o guardarla en el sistema de archivos local.
// 1 - Código QR:
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
#if NET461_OR_GREATER || JAVA
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.EAN13.jpg");
#elif NET5_0_OR_GREATER
using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "FieldOptions.BarcodeGenerator.EAN13.jpg"))
{
    img.Encode(fs, SKEncodedImageFormat.Jpeg, 100);
}
#endif
builder.InsertImage(img);

// 3 - Código de barras CODE39:
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

// 4 - Código de barras ITF14:
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

### Ver también

* class [BarcodeParameters](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
