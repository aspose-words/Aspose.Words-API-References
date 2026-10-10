---
title: "BarcodeParameters"
linktitle: "BarcodeParameters"
second_title: "Aspose.Words für Java"
description: "Container-Klasse für Barcode-Parameter, die an BarcodeGenerator in Java weitergegeben werden."
type: docs
weight: 34
url: /de/java/com.aspose.words/barcodeparameters/
---

**Inheritance:**
java.lang.Object
```
public class BarcodeParameters
```

Containerklasse für Barcode-Parameter, die an BarcodeGenerator weitergereicht werden.

Weitere Informationen finden Sie im Dokumentationsartikel [ Working with Fields ][Working with Fields].

 **Remarks:** 

Der Satz von Parametern entspricht den DISPLAYBARCODE-Feldoptionen. Siehe die genaue Liste unter [ ][Link 1]

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getAddStartStopChar()](#getAddStartStopChar) | Ob Start-/Stopp‑Zeichen für die Barcode‑Typen NW7 und CODE39 hinzugefügt werden sollen. |
| [getBackgroundColor()](#getBackgroundColor) | Barcode-Hintergrundfarbe (0x000000 - 0xFFFFFF) |
| [getBarcodeType()](#getBarcodeType) | Barcode-Typ. |
| [getBarcodeValue()](#getBarcodeValue) | Zu codierende Daten. |
| [getCaseCodeStyle()](#getCaseCodeStyle) | Stil eines Case Code für den Barcode-Typ ITF14. |
| [getDisplayText()](#getDisplayText) | Ob Barcode‑Daten (Text) zusammen mit dem Bild angezeigt werden sollen. |
| [getErrorCorrectionLevel()](#getErrorCorrectionLevel) | Fehlerkorrekturstufe des QR-Codes. |
| [getFacingIdentificationMark()](#getFacingIdentificationMark) | Typ einer Facing Identification Mark (FIM). |
| [getFixCheckDigit()](#getFixCheckDigit) | Ob die Prüfziffer korrigiert werden soll, wenn sie ungültig ist. |
| [getForegroundColor()](#getForegroundColor) | Barcode-Vordergrundfarbe (0x000000 - 0xFFFFFF) |
| [getPosCodeStyle()](#getPosCodeStyle) | Style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). |
| [getPostalAddress()](#getPostalAddress) | Barcode-Postadresse. |
| [getScalingFactor()](#getScalingFactor) | Skalierungsfaktor für das Symbol. |
| [getSymbolHeight()](#getSymbolHeight) | Barcode-Bildhöhe (in Twips - 1/1440 Zoll) |
| [getSymbolRotation()](#getSymbolRotation) | Rotation des Barcode-Symbols. |
| [isBookmark()](#isBookmark) | Ob [getPostalAddress()](../../com.aspose.words/barcodeparameters/\#getPostalAddress) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters/\#setPostalAddress-java.lang.String) der Name eines Lesezeichens ist. |
| [isBookmark(boolean value)](#isBookmark-boolean) | Ob [getPostalAddress()](../../com.aspose.words/barcodeparameters/\#getPostalAddress) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters/\#setPostalAddress-java.lang.String) der Name eines Lesezeichens ist. |
| [isUSPostalAddress()](#isUSPostalAddress) | Ob [getPostalAddress()](../../com.aspose.words/barcodeparameters/\#getPostalAddress) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters/\#setPostalAddress-java.lang.String) ein US-Postfach ist. |
| [isUSPostalAddress(boolean value)](#isUSPostalAddress-boolean) | Ob [getPostalAddress()](../../com.aspose.words/barcodeparameters/\#getPostalAddress) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters/\#setPostalAddress-java.lang.String) ein US-Postfach ist. |
| [setAddStartStopChar(boolean value)](#setAddStartStopChar-boolean) | Ob Start-/Stopp‑Zeichen für die Barcode‑Typen NW7 und CODE39 hinzugefügt werden sollen. |
| [setBackgroundColor(String value)](#setBackgroundColor-java.lang.String) | Barcode-Hintergrundfarbe (0x000000 - 0xFFFFFF) |
| [setBarcodeType(String value)](#setBarcodeType-java.lang.String) | Barcode-Typ. |
| [setBarcodeValue(String value)](#setBarcodeValue-java.lang.String) | Zu codierende Daten. |
| [setCaseCodeStyle(String value)](#setCaseCodeStyle-java.lang.String) | Stil eines Case Code für den Barcode-Typ ITF14. |
| [setDisplayText(boolean value)](#setDisplayText-boolean) | Ob Barcode‑Daten (Text) zusammen mit dem Bild angezeigt werden sollen. |
| [setErrorCorrectionLevel(String value)](#setErrorCorrectionLevel-java.lang.String) | Fehlerkorrekturstufe des QR-Codes. |
| [setFacingIdentificationMark(String value)](#setFacingIdentificationMark-java.lang.String) | Typ einer Facing Identification Mark (FIM). |
| [setFixCheckDigit(boolean value)](#setFixCheckDigit-boolean) | Ob die Prüfziffer korrigiert werden soll, wenn sie ungültig ist. |
| [setForegroundColor(String value)](#setForegroundColor-java.lang.String) | Barcode-Vordergrundfarbe (0x000000 - 0xFFFFFF) |
| [setPosCodeStyle(String value)](#setPosCodeStyle-java.lang.String) | Style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). |
| [setPostalAddress(String value)](#setPostalAddress-java.lang.String) | Barcode-Postadresse. |
| [setScalingFactor(String value)](#setScalingFactor-java.lang.String) | Skalierungsfaktor für das Symbol. |
| [setSymbolHeight(String value)](#setSymbolHeight-java.lang.String) | Barcode-Bildhöhe (in Twips - 1/1440 Zoll) |
| [setSymbolRotation(String value)](#setSymbolRotation-java.lang.String) | Rotation des Barcode-Symbols. |
### getAddStartStopChar() {#getAddStartStopChar}
```
public boolean getAddStartStopChar()
```


Ob Start-/Stopp‑Zeichen für die Barcode‑Typen NW7 und CODE39 hinzugefügt werden sollen.

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
boolean - Der entsprechende  boolean  Wert.
### getBackgroundColor() {#getBackgroundColor}
```
public String getBackgroundColor()
```


Barcode-Hintergrundfarbe (0x000000 - 0xFFFFFF)

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
java.lang.String - Der entsprechende java.lang.String-Wert.
### getBarcodeType() {#getBarcodeType}
```
public String getBarcodeType()
```


Barcode-Typ.

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
java.lang.String - Der entsprechende java.lang.String-Wert.
### getBarcodeValue() {#getBarcodeValue}
```
public String getBarcodeValue()
```


Zu codierende Daten.

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
java.lang.String - Der entsprechende java.lang.String-Wert.
### getCaseCodeStyle() {#getCaseCodeStyle}
```
public String getCaseCodeStyle()
```


Stil eines Case Code für den Barcode-Typ ITF14. Gültige Werte sind [STD|EXT|ADD]

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
java.lang.String - Der entsprechende java.lang.String-Wert.
### getDisplayText() {#getDisplayText}
```
public boolean getDisplayText()
```


Ob Barcode‑Daten (Text) zusammen mit dem Bild angezeigt werden sollen.

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
boolean - Der entsprechende  boolean  Wert.
### getErrorCorrectionLevel() {#getErrorCorrectionLevel}
```
public String getErrorCorrectionLevel()
```


Fehlerkorrekturstufe des QR-Codes. Gültige Werte sind [0, 3].

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
java.lang.String - Der entsprechende java.lang.String-Wert.
### getFacingIdentificationMark() {#getFacingIdentificationMark}
```
public String getFacingIdentificationMark()
```


Typ einer Facing Identification Mark (FIM).

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
java.lang.String - Der entsprechende java.lang.String-Wert.
### getFixCheckDigit() {#getFixCheckDigit}
```
public boolean getFixCheckDigit()
```


Ob die Prüfziffer korrigiert werden soll, wenn sie ungültig ist.

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
boolean - Der entsprechende  boolean  Wert.
### getForegroundColor() {#getForegroundColor}
```
public String getForegroundColor()
```


Barcode-Vordergrundfarbe (0x000000 - 0xFFFFFF)

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
java.lang.String - Der entsprechende java.lang.String-Wert.
### getPosCodeStyle() {#getPosCodeStyle}
```
public String getPosCodeStyle()
```


Stil eines Point-of-Sale-Barcodes (Barcode-Typen UPCA|UPCE|EAN13|EAN8). Die gültigen Werte (Groß-/Kleinschreibung ignorierend) sind [STD|SUP2|SUP5|CASE].

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
java.lang.String - Der entsprechende java.lang.String-Wert.
### getPostalAddress() {#getPostalAddress}
```
public String getPostalAddress()
```


Barcode-Postadresse.

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
java.lang.String - Der entsprechende java.lang.String-Wert.
### getScalingFactor() {#getScalingFactor}
```
public String getScalingFactor()
```


Skalierungsfaktor für das Symbol. Der Wert ist in ganzen Prozentpunkten angegeben und die gültigen Werte sind [10, 1000].

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
java.lang.String - Der entsprechende java.lang.String-Wert.
### getSymbolHeight() {#getSymbolHeight}
```
public String getSymbolHeight()
```


Barcode-Bildhöhe (in Twips - 1/1440 Zoll)

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
java.lang.String - Der entsprechende java.lang.String-Wert.
### getSymbolRotation() {#getSymbolRotation}
```
public String getSymbolRotation()
```


Drehung des Barcode-Symbols. Gültige Werte sind [0, 3].

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
java.lang.String - Der entsprechende java.lang.String-Wert.
### isBookmark() {#isBookmark}
```
public boolean isBookmark()
```


Ob [getPostalAddress()](../../com.aspose.words/barcodeparameters/\#getPostalAddress) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters/\#setPostalAddress-java.lang.String) der Name eines Lesezeichens ist.

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
boolean - Der entsprechende  boolean  Wert.
### isBookmark(boolean value) {#isBookmark-boolean}
```
public void isBookmark(boolean value)
```


Ob [getPostalAddress()](../../com.aspose.words/barcodeparameters/\#getPostalAddress) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters/\#setPostalAddress-java.lang.String) der Name eines Lesezeichens ist.

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### isUSPostalAddress() {#isUSPostalAddress}
```
public boolean isUSPostalAddress()
```


Ob [getPostalAddress()](../../com.aspose.words/barcodeparameters/\#getPostalAddress) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters/\#setPostalAddress-java.lang.String) eine US-Postadresse ist.

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
boolean - Der entsprechende  boolean  Wert.
### isUSPostalAddress(boolean value) {#isUSPostalAddress-boolean}
```
public void isUSPostalAddress(boolean value)
```


Ob [getPostalAddress()](../../com.aspose.words/barcodeparameters/\#getPostalAddress) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters/\#setPostalAddress-java.lang.String) eine US-Postadresse ist.

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setAddStartStopChar(boolean value) {#setAddStartStopChar-boolean}
```
public void setAddStartStopChar(boolean value)
```


Ob Start-/Stopp‑Zeichen für die Barcode‑Typen NW7 und CODE39 hinzugefügt werden sollen.

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setBackgroundColor(String value) {#setBackgroundColor-java.lang.String}
```
public void setBackgroundColor(String value)
```


Barcode-Hintergrundfarbe (0x000000 - 0xFFFFFF)

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setBarcodeType(String value) {#setBarcodeType-java.lang.String}
```
public void setBarcodeType(String value)
```


Barcode-Typ.

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setBarcodeValue(String value) {#setBarcodeValue-java.lang.String}
```
public void setBarcodeValue(String value)
```


Zu codierende Daten.

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setCaseCodeStyle(String value) {#setCaseCodeStyle-java.lang.String}
```
public void setCaseCodeStyle(String value)
```


Stil eines Case Code für den Barcode-Typ ITF14. Gültige Werte sind [STD|EXT|ADD]

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setDisplayText(boolean value) {#setDisplayText-boolean}
```
public void setDisplayText(boolean value)
```


Ob Barcode‑Daten (Text) zusammen mit dem Bild angezeigt werden sollen.

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setErrorCorrectionLevel(String value) {#setErrorCorrectionLevel-java.lang.String}
```
public void setErrorCorrectionLevel(String value)
```


Fehlerkorrekturstufe des QR-Codes. Gültige Werte sind [0, 3].

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setFacingIdentificationMark(String value) {#setFacingIdentificationMark-java.lang.String}
```
public void setFacingIdentificationMark(String value)
```


Typ einer Facing Identification Mark (FIM).

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setFixCheckDigit(boolean value) {#setFixCheckDigit-boolean}
```
public void setFixCheckDigit(boolean value)
```


Ob die Prüfziffer korrigiert werden soll, wenn sie ungültig ist.

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setForegroundColor(String value) {#setForegroundColor-java.lang.String}
```
public void setForegroundColor(String value)
```


Barcode-Vordergrundfarbe (0x000000 - 0xFFFFFF)

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setPosCodeStyle(String value) {#setPosCodeStyle-java.lang.String}
```
public void setPosCodeStyle(String value)
```


Stil eines Point-of-Sale-Barcodes (Barcode-Typen UPCA|UPCE|EAN13|EAN8). Die gültigen Werte (Groß-/Kleinschreibung ignorierend) sind [STD|SUP2|SUP5|CASE].

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setPostalAddress(String value) {#setPostalAddress-java.lang.String}
```
public void setPostalAddress(String value)
```


Barcode-Postadresse.

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setScalingFactor(String value) {#setScalingFactor-java.lang.String}
```
public void setScalingFactor(String value)
```


Skalierungsfaktor für das Symbol. Der Wert ist in ganzen Prozentpunkten angegeben und die gültigen Werte sind [10, 1000].

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setSymbolHeight(String value) {#setSymbolHeight-java.lang.String}
```
public void setSymbolHeight(String value)
```


Barcode-Bildhöhe (in Twips - 1/1440 Zoll)

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setSymbolRotation(String value) {#setSymbolRotation-java.lang.String}
```
public void setSymbolRotation(String value)
```


Drehung des Barcode-Symbols. Gültige Werte sind [0, 3].

 **Examples:** 

Zeigt, wie man einen Barcode‑Generator verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

