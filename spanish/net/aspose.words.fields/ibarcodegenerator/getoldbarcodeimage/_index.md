---
title: IBarcodeGenerator.GetOldBarcodeImage
linktitle: GetOldBarcodeImage
articleTitle: GetOldBarcodeImage
second_title: Aspose.Words para .NET
description: Crea imágenes de códigos de barras antiguos fácilmente con el método GetOldBarcodeImage de iBarcodeGenerator. ¡Personalízalas fácilmente con tus parámetros preferidos!
type: docs
weight: 20
url: /es/net/aspose.words.fields/ibarcodegenerator/getoldbarcodeimage/
---
## IBarcodeGenerator.GetOldBarcodeImage method

Generar imagen de código de barras utilizando el conjunto de parámetros (para el campo de código de barras antiguo).

```csharp
public Image GetOldBarcodeImage(BarcodeParameters parameters)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| parameters | BarcodeParameters | El conjunto de parámetros |

### Valor_devuelto

Imagen que representa el código de barras generado.

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

* class [BarcodeParameters](../../barcodeparameters/)
* interface [IBarcodeGenerator](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
