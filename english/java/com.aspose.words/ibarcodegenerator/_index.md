---
title: IBarcodeGenerator
second_title: Aspose.Words for Java API Reference
description: Public interface for barcode custom generator.
type: docs
weight: 635
url: /java/com.aspose.words/ibarcodegenerator/
---
```
public interface IBarcodeGenerator
```

Public interface for barcode custom generator. Implementation should be provided by user. Generator instance should be passed through the [FieldOptions.getBarcodeGenerator()](../../com.aspose.words/fieldoptions\#getBarcodeGenerator) / [FieldOptions.setBarcodeGenerator(com.aspose.words.IBarcodeGenerator)](../../com.aspose.words/fieldoptions\#setBarcodeGenerator-com.aspose.words.IBarcodeGenerator) property.
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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| parameters | [BarcodeParameters](../../com.aspose.words/barcodeparameters) | The set of parameters |

**Returns:**
java.awt.image.BufferedImage - Image representing generated barcode.
### getOldBarcodeImage(BarcodeParameters parameters) {#getOldBarcodeImage-com.aspose.words.BarcodeParameters}
```
public abstract BufferedImage getOldBarcodeImage(BarcodeParameters parameters)
```


Generate barcode image using the set of parameters (for old-fashioned Barcode field).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| parameters | [BarcodeParameters](../../com.aspose.words/barcodeparameters) | The set of parameters |

**Returns:**
java.awt.image.BufferedImage - Image representing generated barcode.
