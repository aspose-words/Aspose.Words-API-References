---
title: "BarcodeParameters"
linktitle: "BarcodeParameters"
second_title: "Aspose.Words Java için"
description: "Java'da BarcodeGenerator'a iletilmek üzere barkod parametreleri için kapsayıcı sınıf."
type: docs
weight: 34
url: /tr/java/com.aspose.words/barcodeparameters/
---

**Inheritance:**
java.lang.Object
```
public class BarcodeParameters
```

BarcodeGenerator'a aktarılacak barkod parametreleri için kapsayıcı sınıf.

Daha fazla bilgi için, [ Working with Fields ][Working with Fields] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Parametre kümesi DISPLAYBARCODE alan seçeneklerine göre belirlenir. Tam listeyi [ ][Link 1] adresinde görebilirsiniz.

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
[Link 1]: https://msdn.microsoft.com/en-us/library/hh745901%28v=office.12%29.aspx
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getAddStartStopChar()](#getAddStartStopChar) | NW7 ve CODE39 barkod tipleri için Başlat/Durdur karakterlerinin eklenip eklenmeyeceği. |
| [getBackgroundColor()](#getBackgroundColor) | Barkod arka plan rengi (0x000000 - 0xFFFFFF) |
| [getBarcodeType()](#getBarcodeType) | Barkod türü. |
| [getBarcodeValue()](#getBarcodeValue) | Kodlanacak veri. |
| [getCaseCodeStyle()](#getCaseCodeStyle) | ITF14 barkod türü için Kutu Kodu stilı. |
| [getDisplayText()](#getDisplayText) | Barkod verisinin (metin) görüntüyle birlikte gösterilip gösterilmeyeceği. |
| [getErrorCorrectionLevel()](#getErrorCorrectionLevel) | QR Kodunun hata düzeltme seviyesi. |
| [getFacingIdentificationMark()](#getFacingIdentificationMark) | Yüzey Tanımlama İşareti (FIM) tipi. |
| [getFixCheckDigit()](#getFixCheckDigit) | Kontrol rakamı geçersizse düzeltip düzeltmeyeceği. |
| [getForegroundColor()](#getForegroundColor) | Barkod ön plan rengi (0x000000 - 0xFFFFFF) |
| [getPosCodeStyle()](#getPosCodeStyle) | Style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). |
| [getPostalAddress()](#getPostalAddress) | Barkod posta adresi. |
| [getScalingFactor()](#getScalingFactor) | Sembol için ölçek faktörü. |
| [getSymbolHeight()](#getSymbolHeight) | Barkod görüntü yüksekliği (twip cinsinden - 1/1440 inç) |
| [getSymbolRotation()](#getSymbolRotation) | Barkod sembolünün dönüşü. |
| [isBookmark()](#isBookmark) | Bu [getPostalAddress()](../../com.aspose.words/barcodeparameters/\#getPostalAddress) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters/\#setPostalAddress-java.lang.String) bir yer işareti adıdır. |
| [isBookmark(boolean value)](#isBookmark-boolean) | Bu [getPostalAddress()](../../com.aspose.words/barcodeparameters/\#getPostalAddress) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters/\#setPostalAddress-java.lang.String) bir yer işareti adıdır. |
| [isUSPostalAddress()](#isUSPostalAddress) | Bu [getPostalAddress()](../../com.aspose.words/barcodeparameters/\#getPostalAddress) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters/\#setPostalAddress-java.lang.String) bir ABD adresi mi? |
| [isUSPostalAddress(boolean value)](#isUSPostalAddress-boolean) | Bu [getPostalAddress()](../../com.aspose.words/barcodeparameters/\#getPostalAddress) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters/\#setPostalAddress-java.lang.String) bir ABD adresi mi? |
| [setAddStartStopChar(boolean value)](#setAddStartStopChar-boolean) | NW7 ve CODE39 barkod tipleri için Başlat/Durdur karakterlerinin eklenip eklenmeyeceği. |
| [setBackgroundColor(String value)](#setBackgroundColor-java.lang.String) | Barkod arka plan rengi (0x000000 - 0xFFFFFF) |
| [setBarcodeType(String value)](#setBarcodeType-java.lang.String) | Barkod türü. |
| [setBarcodeValue(String value)](#setBarcodeValue-java.lang.String) | Kodlanacak veri. |
| [setCaseCodeStyle(String value)](#setCaseCodeStyle-java.lang.String) | ITF14 barkod türü için Kutu Kodu stilı. |
| [setDisplayText(boolean value)](#setDisplayText-boolean) | Barkod verisinin (metin) görüntüyle birlikte gösterilip gösterilmeyeceği. |
| [setErrorCorrectionLevel(String value)](#setErrorCorrectionLevel-java.lang.String) | QR Kodunun hata düzeltme seviyesi. |
| [setFacingIdentificationMark(String value)](#setFacingIdentificationMark-java.lang.String) | Yüzey Tanımlama İşareti (FIM) tipi. |
| [setFixCheckDigit(boolean value)](#setFixCheckDigit-boolean) | Kontrol rakamı geçersizse düzeltip düzeltmeyeceği. |
| [setForegroundColor(String value)](#setForegroundColor-java.lang.String) | Barkod ön plan rengi (0x000000 - 0xFFFFFF) |
| [setPosCodeStyle(String value)](#setPosCodeStyle-java.lang.String) | Style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). |
| [setPostalAddress(String value)](#setPostalAddress-java.lang.String) | Barkod posta adresi. |
| [setScalingFactor(String value)](#setScalingFactor-java.lang.String) | Sembol için ölçek faktörü. |
| [setSymbolHeight(String value)](#setSymbolHeight-java.lang.String) | Barkod görüntü yüksekliği (twip cinsinden - 1/1440 inç) |
| [setSymbolRotation(String value)](#setSymbolRotation-java.lang.String) | Barkod sembolünün dönüşü. |
### getAddStartStopChar() {#getAddStartStopChar}
```
public boolean getAddStartStopChar()
```


NW7 ve CODE39 barkod tipleri için Başlat/Durdur karakterlerinin eklenip eklenmeyeceği.

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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

**Returns:**
boolean - İlgili  boolean  değeri.
### getBackgroundColor() {#getBackgroundColor}
```
public String getBackgroundColor()
```


Barkod arka plan rengi (0x000000 - 0xFFFFFF)

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getBarcodeType() {#getBarcodeType}
```
public String getBarcodeType()
```


Barkod türü.

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getBarcodeValue() {#getBarcodeValue}
```
public String getBarcodeValue()
```


Kodlanacak veri.

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getCaseCodeStyle() {#getCaseCodeStyle}
```
public String getCaseCodeStyle()
```


ITF14 barkod tipi için Case Code stilidir. Geçerli değerler [STD|EXT|ADD]

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getDisplayText() {#getDisplayText}
```
public boolean getDisplayText()
```


Barkod verisinin (metin) görüntüyle birlikte gösterilip gösterilmeyeceği.

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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

**Returns:**
boolean - İlgili  boolean  değeri.
### getErrorCorrectionLevel() {#getErrorCorrectionLevel}
```
public String getErrorCorrectionLevel()
```


QR Kodunun hata düzeltme seviyesi. Geçerli değerler [0, 3].

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getFacingIdentificationMark() {#getFacingIdentificationMark}
```
public String getFacingIdentificationMark()
```


Yüzey Tanımlama İşareti (FIM) tipi.

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getFixCheckDigit() {#getFixCheckDigit}
```
public boolean getFixCheckDigit()
```


Kontrol rakamı geçersizse düzeltip düzeltmeyeceği.

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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

**Returns:**
boolean - İlgili  boolean  değeri.
### getForegroundColor() {#getForegroundColor}
```
public String getForegroundColor()
```


Barkod ön plan rengi (0x000000 - 0xFFFFFF)

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getPosCodeStyle() {#getPosCodeStyle}
```
public String getPosCodeStyle()
```


Satış Noktası barkodu (barkod tipleri UPCA|UPCE|EAN13|EAN8) stilidir. Geçerli değerler (büyük/küçük harf duyarsız) [STD|SUP2|SUP5|CASE].

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getPostalAddress() {#getPostalAddress}
```
public String getPostalAddress()
```


Barkod posta adresi.

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getScalingFactor() {#getScalingFactor}
```
public String getScalingFactor()
```


Sembol için ölçekleme faktörü. Değer tam yüzde puanlarıdır ve geçerli değerler [10, 1000].

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getSymbolHeight() {#getSymbolHeight}
```
public String getSymbolHeight()
```


Barkod görüntü yüksekliği (twip cinsinden - 1/1440 inç)

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getSymbolRotation() {#getSymbolRotation}
```
public String getSymbolRotation()
```


Barkod sembolünün dönüşü. Geçerli değerler [0, 3].

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### isBookmark() {#isBookmark}
```
public boolean isBookmark()
```


Bu [getPostalAddress()](../../com.aspose.words/barcodeparameters/\#getPostalAddress) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters/\#setPostalAddress-java.lang.String) bir yer işareti adıdır.

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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

**Returns:**
boolean - İlgili  boolean  değeri.
### isBookmark(boolean value) {#isBookmark-boolean}
```
public void isBookmark(boolean value)
```


Bu [getPostalAddress()](../../com.aspose.words/barcodeparameters/\#getPostalAddress) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters/\#setPostalAddress-java.lang.String) bir yer işareti adıdır.

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### isUSPostalAddress() {#isUSPostalAddress}
```
public boolean isUSPostalAddress()
```


Bu [getPostalAddress()](../../com.aspose.words/barcodeparameters/\#getPostalAddress) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters/\#setPostalAddress-java.lang.String) bir ABD posta adresi mi?

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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

**Returns:**
boolean - İlgili  boolean  değeri.
### isUSPostalAddress(boolean value) {#isUSPostalAddress-boolean}
```
public void isUSPostalAddress(boolean value)
```


Bu [getPostalAddress()](../../com.aspose.words/barcodeparameters/\#getPostalAddress) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters/\#setPostalAddress-java.lang.String) bir ABD posta adresi mi?

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setAddStartStopChar(boolean value) {#setAddStartStopChar-boolean}
```
public void setAddStartStopChar(boolean value)
```


NW7 ve CODE39 barkod tipleri için Başlat/Durdur karakterlerinin eklenip eklenmeyeceği.

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setBackgroundColor(String value) {#setBackgroundColor-java.lang.String}
```
public void setBackgroundColor(String value)
```


Barkod arka plan rengi (0x000000 - 0xFFFFFF)

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setBarcodeType(String value) {#setBarcodeType-java.lang.String}
```
public void setBarcodeType(String value)
```


Barkod türü.

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setBarcodeValue(String value) {#setBarcodeValue-java.lang.String}
```
public void setBarcodeValue(String value)
```


Kodlanacak veri.

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setCaseCodeStyle(String value) {#setCaseCodeStyle-java.lang.String}
```
public void setCaseCodeStyle(String value)
```


ITF14 barkod tipi için Case Code stilidir. Geçerli değerler [STD|EXT|ADD]

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setDisplayText(boolean value) {#setDisplayText-boolean}
```
public void setDisplayText(boolean value)
```


Barkod verisinin (metin) görüntüyle birlikte gösterilip gösterilmeyeceği.

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setErrorCorrectionLevel(String value) {#setErrorCorrectionLevel-java.lang.String}
```
public void setErrorCorrectionLevel(String value)
```


QR Kodunun hata düzeltme seviyesi. Geçerli değerler [0, 3].

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setFacingIdentificationMark(String value) {#setFacingIdentificationMark-java.lang.String}
```
public void setFacingIdentificationMark(String value)
```


Yüzey Tanımlama İşareti (FIM) tipi.

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setFixCheckDigit(boolean value) {#setFixCheckDigit-boolean}
```
public void setFixCheckDigit(boolean value)
```


Kontrol rakamı geçersizse düzeltip düzeltmeyeceği.

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setForegroundColor(String value) {#setForegroundColor-java.lang.String}
```
public void setForegroundColor(String value)
```


Barkod ön plan rengi (0x000000 - 0xFFFFFF)

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setPosCodeStyle(String value) {#setPosCodeStyle-java.lang.String}
```
public void setPosCodeStyle(String value)
```


Satış Noktası barkodu (barkod tipleri UPCA|UPCE|EAN13|EAN8) stilidir. Geçerli değerler (büyük/küçük harf duyarsız) [STD|SUP2|SUP5|CASE].

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setPostalAddress(String value) {#setPostalAddress-java.lang.String}
```
public void setPostalAddress(String value)
```


Barkod posta adresi.

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setScalingFactor(String value) {#setScalingFactor-java.lang.String}
```
public void setScalingFactor(String value)
```


Sembol için ölçekleme faktörü. Değer tam yüzde puanlarıdır ve geçerli değerler [10, 1000].

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setSymbolHeight(String value) {#setSymbolHeight-java.lang.String}
```
public void setSymbolHeight(String value)
```


Barkod görüntü yüksekliği (twip cinsinden - 1/1440 inç)

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setSymbolRotation(String value) {#setSymbolRotation-java.lang.String}
```
public void setSymbolRotation(String value)
```


Barkod sembolünün dönüşü. Geçerli değerler [0, 3].

 **Examples:** 

Barkod üreticisinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

