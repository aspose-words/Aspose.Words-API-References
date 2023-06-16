---
title: IBarcodeGenerator
linktitle: IBarcodeGenerator
second_title: Aspose.Words for Java
description: Public interface for barcode custom generator in Java.
type: docs
weight: 656
url: /java/com.aspose.words/ibarcodegenerator/
---
```
public interface IBarcodeGenerator
```

Public interface for barcode custom generator. Implementation should be provided by user.

 **Remarks:** 

Generator instance should be passed through the [FieldOptions.getBarcodeGenerator()](../../com.aspose.words/fieldoptions/\#getBarcodeGenerator) / [FieldOptions.setBarcodeGenerator(com.aspose.words.IBarcodeGenerator)](../../com.aspose.words/fieldoptions/\#setBarcodeGenerator-com.aspose.words.IBarcodeGenerator) property.

 **Examples:** 

Shows how to use a barcode generator.

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
## Methods

| Method | Description |
| --- | --- |
| [getBarcodeImage(BarcodeParameters parameters)](#getBarcodeImage-com.aspose.words.BarcodeParameters) | Generate barcode image using the set of parameters (for DisplayBarcode field). |
| [getOldBarcodeImage(BarcodeParameters parameters)](#getOldBarcodeImage-com.aspose.words.BarcodeParameters) | Generate barcode image using the set of parameters (for old-fashioned Barcode field). |
### getBarcodeImage(BarcodeParameters parameters) {#getBarcodeImage-com.aspose.words.BarcodeParameters}
```
public abstract BufferedImage getBarcodeImage(BarcodeParameters parameters)
```


Generate barcode image using the set of parameters (for DisplayBarcode field).

 **Examples:** 

Shows how to use a barcode generator.

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
| Parameter | Type | Description |
| --- | --- | --- |
| parameters | [BarcodeParameters](../../com.aspose.words/barcodeparameters/) | The set of parameters |

**Returns:**
java.awt.image.BufferedImage - Image representing generated barcode.
### getOldBarcodeImage(BarcodeParameters parameters) {#getOldBarcodeImage-com.aspose.words.BarcodeParameters}
```
public abstract BufferedImage getOldBarcodeImage(BarcodeParameters parameters)
```


Generate barcode image using the set of parameters (for old-fashioned Barcode field).

 **Examples:** 

Shows how to use a barcode generator.

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
| Parameter | Type | Description |
| --- | --- | --- |
| parameters | [BarcodeParameters](../../com.aspose.words/barcodeparameters/) | The set of parameters |

**Returns:**
java.awt.image.BufferedImage - Image representing generated barcode.
