---
title: "IBarcodeGenerator"
linktitle: "IBarcodeGenerator"
second_title: "Aspose.Words para Java"
description: "Interfaz pública para el generador personalizado de códigos de barras en Java."
type: docs
weight: 752
url: /es/java/com.aspose.words/ibarcodegenerator/
---
```
public interface IBarcodeGenerator
```

Interfaz pública para el generador personalizado de códigos de barras. La implementación debe ser proporcionada por el usuario.

 **Remarks:** 

La instancia del generador debe pasarse a través de la propiedad [FieldOptions.getBarcodeGenerator()](../../com.aspose.words/fieldoptions/\#getBarcodeGenerator) / [FieldOptions.setBarcodeGenerator(com.aspose.words.IBarcodeGenerator)](../../com.aspose.words/fieldoptions/\#setBarcodeGenerator-com.aspose.words.IBarcodeGenerator).

 **Examples:** 

Muestra cómo usar un generador de códigos de barras.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 // We can use a custom IBarcodeGenerator implementation to generate barcodes,
 // and then insert them into the document as images.
 doc.getFieldOptions().setBarcodeGenerator(new CustomBarcodeGenerator());

 // Below are four examples of different barcode types that we can create using our generator.
 // For each barcode, we specify a new set of barcode parameters, and then generate the image.
 // Afterwards, we can insert the image into the document, or save it to the local file system.
 // 1 -  QR code:
 BarcodeParameters barcodeParameters = new BarcodeParameters();
 {
     barcodeParameters.setBarcodeType("QR");
     barcodeParameters.setBarcodeValue("ABC123");
     barcodeParameters.setBackgroundColor("0xF8BD69");
     barcodeParameters.setForegroundColor("0xB5413B");
     barcodeParameters.setErrorCorrectionLevel("3");
     barcodeParameters.setScalingFactor("250");
     barcodeParameters.setSymbolHeight("1000");
     barcodeParameters.setSymbolRotation("0");
 }

 BufferedImage img = doc.getFieldOptions().getBarcodeGenerator().getBarcodeImage(barcodeParameters);
 ImageIO.write(img, "jpg", new File(getArtifactsDir() + "FieldOptions.BarcodeGenerator.QR.jpg"));

 builder.insertImage(img);

 // 2 -  EAN13 barcode:
 barcodeParameters = new BarcodeParameters();
 {
     barcodeParameters.setBarcodeType("EAN13");
     barcodeParameters.setBarcodeValue("501234567890");
     barcodeParameters.setDisplayText(true);
     barcodeParameters.setPosCodeStyle("CASE");
     barcodeParameters.setFixCheckDigit(true);
 }

 img = doc.getFieldOptions().getBarcodeGenerator().getBarcodeImage(barcodeParameters);
 ImageIO.write(img, "jpg", new File(getArtifactsDir() + "FieldOptions.BarcodeGenerator.EAN13.jpg"));
 builder.insertImage(img);

 // 3 -  CODE39 barcode:
 barcodeParameters = new BarcodeParameters();
 {
     barcodeParameters.setBarcodeType("CODE39");
     barcodeParameters.setBarcodeValue("12345ABCDE");
     barcodeParameters.setAddStartStopChar(true);
 }

 img = doc.getFieldOptions().getBarcodeGenerator().getBarcodeImage(barcodeParameters);
 ImageIO.write(img, "jpg", new File(getArtifactsDir() + "FieldOptions.BarcodeGenerator.CODE39.jpg"));
 builder.insertImage(img);

 // 4 -  ITF14 barcode:
 barcodeParameters = new BarcodeParameters();
 {
     barcodeParameters.setBarcodeType("ITF14");
     barcodeParameters.setBarcodeValue("09312345678907");
     barcodeParameters.setCaseCodeStyle("STD");
 }

 img = doc.getFieldOptions().getBarcodeGenerator().getBarcodeImage(barcodeParameters);
 ImageIO.write(img, "jpg", new File(getArtifactsDir() + "FieldOptions.BarcodeGenerator.ITF14.jpg"));
 builder.insertImage(img);

 doc.save(getArtifactsDir() + "FieldOptions.BarcodeGenerator.docx");
 
```
## Métodos

| Método | Descripción |
| --- | --- |
| [getBarcodeImage(BarcodeParameters parameters)](#getBarcodeImage-com.aspose.words.BarcodeParameters) | Genera una imagen de código de barras usando el conjunto de parámetros (para el campo DisplayBarcode). |
| [getOldBarcodeImage(BarcodeParameters parameters)](#getOldBarcodeImage-com.aspose.words.BarcodeParameters) | Genera una imagen de código de barras usando el conjunto de parámetros (para el campo Barcode tradicional). |
### getBarcodeImage(BarcodeParameters parameters) {#getBarcodeImage-com.aspose.words.BarcodeParameters}
```
public abstract BufferedImage getBarcodeImage(BarcodeParameters parameters)
```


Genera una imagen de código de barras usando el conjunto de parámetros (para el campo DisplayBarcode).

 **Remarks:** 

Los formatos de imagen compatibles son Bmp, Emf, Gif, Jpeg, Png, Tiff, Wmf, Pict, Ico, WebP, Svg.

 **Examples:** 

Muestra cómo usar un generador de códigos de barras.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 // We can use a custom IBarcodeGenerator implementation to generate barcodes,
 // and then insert them into the document as images.
 doc.getFieldOptions().setBarcodeGenerator(new CustomBarcodeGenerator());

 // Below are four examples of different barcode types that we can create using our generator.
 // For each barcode, we specify a new set of barcode parameters, and then generate the image.
 // Afterwards, we can insert the image into the document, or save it to the local file system.
 // 1 -  QR code:
 BarcodeParameters barcodeParameters = new BarcodeParameters();
 {
     barcodeParameters.setBarcodeType("QR");
     barcodeParameters.setBarcodeValue("ABC123");
     barcodeParameters.setBackgroundColor("0xF8BD69");
     barcodeParameters.setForegroundColor("0xB5413B");
     barcodeParameters.setErrorCorrectionLevel("3");
     barcodeParameters.setScalingFactor("250");
     barcodeParameters.setSymbolHeight("1000");
     barcodeParameters.setSymbolRotation("0");
 }

 BufferedImage img = doc.getFieldOptions().getBarcodeGenerator().getBarcodeImage(barcodeParameters);
 ImageIO.write(img, "jpg", new File(getArtifactsDir() + "FieldOptions.BarcodeGenerator.QR.jpg"));

 builder.insertImage(img);

 // 2 -  EAN13 barcode:
 barcodeParameters = new BarcodeParameters();
 {
     barcodeParameters.setBarcodeType("EAN13");
     barcodeParameters.setBarcodeValue("501234567890");
     barcodeParameters.setDisplayText(true);
     barcodeParameters.setPosCodeStyle("CASE");
     barcodeParameters.setFixCheckDigit(true);
 }

 img = doc.getFieldOptions().getBarcodeGenerator().getBarcodeImage(barcodeParameters);
 ImageIO.write(img, "jpg", new File(getArtifactsDir() + "FieldOptions.BarcodeGenerator.EAN13.jpg"));
 builder.insertImage(img);

 // 3 -  CODE39 barcode:
 barcodeParameters = new BarcodeParameters();
 {
     barcodeParameters.setBarcodeType("CODE39");
     barcodeParameters.setBarcodeValue("12345ABCDE");
     barcodeParameters.setAddStartStopChar(true);
 }

 img = doc.getFieldOptions().getBarcodeGenerator().getBarcodeImage(barcodeParameters);
 ImageIO.write(img, "jpg", new File(getArtifactsDir() + "FieldOptions.BarcodeGenerator.CODE39.jpg"));
 builder.insertImage(img);

 // 4 -  ITF14 barcode:
 barcodeParameters = new BarcodeParameters();
 {
     barcodeParameters.setBarcodeType("ITF14");
     barcodeParameters.setBarcodeValue("09312345678907");
     barcodeParameters.setCaseCodeStyle("STD");
 }

 img = doc.getFieldOptions().getBarcodeGenerator().getBarcodeImage(barcodeParameters);
 ImageIO.write(img, "jpg", new File(getArtifactsDir() + "FieldOptions.BarcodeGenerator.ITF14.jpg"));
 builder.insertImage(img);

 doc.save(getArtifactsDir() + "FieldOptions.BarcodeGenerator.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| parameters | [BarcodeParameters](../../com.aspose.words/barcodeparameters/) | El conjunto de parámetros |

**Returns:**
java.awt.image.BufferedImage - Flujo con datos de imagen que representan el código de barras generado.
### getOldBarcodeImage(BarcodeParameters parameters) {#getOldBarcodeImage-com.aspose.words.BarcodeParameters}
```
public abstract BufferedImage getOldBarcodeImage(BarcodeParameters parameters)
```


Genera una imagen de código de barras usando el conjunto de parámetros (para el campo Barcode tradicional).

 **Remarks:** 

Los formatos de imagen compatibles son Bmp, Emf, Gif, Jpeg, Png, Tiff, Wmf, Pict, Ico, WebP, Svg.

 **Examples:** 

Muestra cómo usar un generador de códigos de barras.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 // We can use a custom IBarcodeGenerator implementation to generate barcodes,
 // and then insert them into the document as images.
 doc.getFieldOptions().setBarcodeGenerator(new CustomBarcodeGenerator());

 // Below are four examples of different barcode types that we can create using our generator.
 // For each barcode, we specify a new set of barcode parameters, and then generate the image.
 // Afterwards, we can insert the image into the document, or save it to the local file system.
 // 1 -  QR code:
 BarcodeParameters barcodeParameters = new BarcodeParameters();
 {
     barcodeParameters.setBarcodeType("QR");
     barcodeParameters.setBarcodeValue("ABC123");
     barcodeParameters.setBackgroundColor("0xF8BD69");
     barcodeParameters.setForegroundColor("0xB5413B");
     barcodeParameters.setErrorCorrectionLevel("3");
     barcodeParameters.setScalingFactor("250");
     barcodeParameters.setSymbolHeight("1000");
     barcodeParameters.setSymbolRotation("0");
 }

 BufferedImage img = doc.getFieldOptions().getBarcodeGenerator().getBarcodeImage(barcodeParameters);
 ImageIO.write(img, "jpg", new File(getArtifactsDir() + "FieldOptions.BarcodeGenerator.QR.jpg"));

 builder.insertImage(img);

 // 2 -  EAN13 barcode:
 barcodeParameters = new BarcodeParameters();
 {
     barcodeParameters.setBarcodeType("EAN13");
     barcodeParameters.setBarcodeValue("501234567890");
     barcodeParameters.setDisplayText(true);
     barcodeParameters.setPosCodeStyle("CASE");
     barcodeParameters.setFixCheckDigit(true);
 }

 img = doc.getFieldOptions().getBarcodeGenerator().getBarcodeImage(barcodeParameters);
 ImageIO.write(img, "jpg", new File(getArtifactsDir() + "FieldOptions.BarcodeGenerator.EAN13.jpg"));
 builder.insertImage(img);

 // 3 -  CODE39 barcode:
 barcodeParameters = new BarcodeParameters();
 {
     barcodeParameters.setBarcodeType("CODE39");
     barcodeParameters.setBarcodeValue("12345ABCDE");
     barcodeParameters.setAddStartStopChar(true);
 }

 img = doc.getFieldOptions().getBarcodeGenerator().getBarcodeImage(barcodeParameters);
 ImageIO.write(img, "jpg", new File(getArtifactsDir() + "FieldOptions.BarcodeGenerator.CODE39.jpg"));
 builder.insertImage(img);

 // 4 -  ITF14 barcode:
 barcodeParameters = new BarcodeParameters();
 {
     barcodeParameters.setBarcodeType("ITF14");
     barcodeParameters.setBarcodeValue("09312345678907");
     barcodeParameters.setCaseCodeStyle("STD");
 }

 img = doc.getFieldOptions().getBarcodeGenerator().getBarcodeImage(barcodeParameters);
 ImageIO.write(img, "jpg", new File(getArtifactsDir() + "FieldOptions.BarcodeGenerator.ITF14.jpg"));
 builder.insertImage(img);

 doc.save(getArtifactsDir() + "FieldOptions.BarcodeGenerator.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| parameters | [BarcodeParameters](../../com.aspose.words/barcodeparameters/) | El conjunto de parámetros |

**Returns:**
java.awt.image.BufferedImage - Flujo con datos de imagen que representan el código de barras generado.
