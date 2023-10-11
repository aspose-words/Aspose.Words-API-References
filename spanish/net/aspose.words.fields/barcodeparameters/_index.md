---
title: Class BarcodeParameters
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fields.BarcodeParameters clase. Clase de contenedor para que los parámetros del código de barras pasen a BarcodeGenerator.
type: docs
weight: 1470
url: /es/net/aspose.words.fields/barcodeparameters/
---
## BarcodeParameters class

Clase de contenedor para que los parámetros del código de barras pasen a BarcodeGenerator.

Para obtener más información, visite el[Trabajar con campos](https://docs.aspose.com/words/net/working-with-fields/) artículo de documentación.

```csharp
public class BarcodeParameters
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [BarcodeParameters](barcodeparameters/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AddStartStopChar](../../aspose.words.fields/barcodeparameters/addstartstopchar/) { get; set; } | Si se deben agregar caracteres de inicio/parada para los tipos de códigos de barras NW7 y CODE39. |
| [BackgroundColor](../../aspose.words.fields/barcodeparameters/backgroundcolor/) { get; set; } | Color de fondo del código de barras (0x000000 - 0xFFFFFF) |
| [BarcodeType](../../aspose.words.fields/barcodeparameters/barcodetype/) { get; set; } | Tipo de código de barras. |
| [BarcodeValue](../../aspose.words.fields/barcodeparameters/barcodevalue/) { get; set; } | Datos a codificar. |
| [CaseCodeStyle](../../aspose.words.fields/barcodeparameters/casecodestyle/) { get; set; } | Estilo de un código de caso para el tipo de código de barras ITF14. Los valores válidos son [STD&#x7C;EXT&#x7C;ADD] |
| [DisplayText](../../aspose.words.fields/barcodeparameters/displaytext/) { get; set; } | Si se muestran datos de código de barras (texto) junto con la imagen. |
| [ErrorCorrectionLevel](../../aspose.words.fields/barcodeparameters/errorcorrectionlevel/) { get; set; } | Nivel de corrección de error del Código QR. Los valores válidos son [0, 3]. |
| [FacingIdentificationMark](../../aspose.words.fields/barcodeparameters/facingidentificationmark/) { get; set; } | Tipo de marca de identificación de frente (FIM). |
| [FixCheckDigit](../../aspose.words.fields/barcodeparameters/fixcheckdigit/) { get; set; } | Si se debe corregir el dígito de control si no es válido. |
| [ForegroundColor](../../aspose.words.fields/barcodeparameters/foregroundcolor/) { get; set; } | Color de primer plano del código de barras (0x000000 - 0xFFFFFF) |
| [IsBookmark](../../aspose.words.fields/barcodeparameters/isbookmark/) { get; set; } | Si[`PostalAddress`](./postaladdress/) es el nombre de un marcador. |
| [IsUSPostalAddress](../../aspose.words.fields/barcodeparameters/isuspostaladdress/) { get; set; } | Si[`PostalAddress`](./postaladdress/) es una dirección postal de EE. UU. |
| [PosCodeStyle](../../aspose.words.fields/barcodeparameters/poscodestyle/) { get; set; } | Estilo de un código de barras de Punto de Venta (tipos de códigos de barras UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). Los valores válidos (sin distinguir entre mayúsculas y minúsculas) son [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE]. |
| [PostalAddress](../../aspose.words.fields/barcodeparameters/postaladdress/) { get; set; } | Dirección postal del código de barras. |
| [ScalingFactor](../../aspose.words.fields/barcodeparameters/scalingfactor/) { get; set; } | Factor de escala para el símbolo. El valor está en puntos porcentuales enteros y los valores válidos son [10, 1000]. |
| [SymbolHeight](../../aspose.words.fields/barcodeparameters/symbolheight/) { get; set; } | Altura de la imagen del código de barras (en twips - 1/1440 pulgadas) |
| [SymbolRotation](../../aspose.words.fields/barcodeparameters/symbolrotation/) { get; set; } | Rotación del símbolo del código de barras. Los valores válidos son [0, 3]. |

### Observaciones

El conjunto de parámetros está de acuerdo con las opciones del campo DISPLAYBARCODE. Vea la lista exacta en[https://msdn.microsoft.com/en-us/library/hh745901(v=office.12).aspx](https://msdn.microsoft.com/en-us/library/hh745901(v=office.12).aspx)

### Ejemplos

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

* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)


