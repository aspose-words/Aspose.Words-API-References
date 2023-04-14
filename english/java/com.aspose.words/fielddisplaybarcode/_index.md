---
title: FieldDisplayBarcode
linktitle: FieldDisplayBarcode
second_title: Aspose.Words for Java API Reference
description: Implements the DISPLAYBARCODE field in Java.
type: docs
weight: 182
url: /java/com.aspose.words/fielddisplaybarcode/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field/)
```
public class FieldDisplayBarcode extends Field
```

Implements the DISPLAYBARCODE field.

To learn more, visit the [ Working with Fields ][Working with Fields] documentation article.

 **Remarks:** 

Inserts a barcode.

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

Shows how to perform a mail merge on QR barcodes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyQRCode" column into QR codes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("QR");
 field.setBarcodeValue("MyQRCode");

 // Apply custom colors and scaling.
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyQRCode QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0",
         field.getFieldCode());
 builder.writeln();

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display a QR code with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyQRCode");
 table.getRows().add(new String[]{"ABC123"});
 table.getRows().add(new String[]{"DEF456"});

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals("DISPLAYBARCODE \"ABC123\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals("DISPLAYBARCODE \"DEF456\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.QR.docx");
 
```


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getAddStartStopChar()](#getAddStartStopChar) | Gets whether to add Start/Stop characters for barcode types NW7 and CODE39. |
| [getBackgroundColor()](#getBackgroundColor) | Gets the background color of the barcode symbol. |
| [getBarcodeType()](#getBarcodeType) | Gets the barcode type (QR, etc.) |
| [getBarcodeValue()](#getBarcodeValue) | Gets the barcode value. |
| [getCaseCodeStyle()](#getCaseCodeStyle) | Gets the style of a Case Code for barcode type ITF14. |
| [getClass()](#getClass) |  |
| [getDisplayResult()](#getDisplayResult) | Gets the text that represents the displayed field result. |
| [getDisplayText()](#getDisplayText) | Gets whether to display barcode data (text) along with image. |
| [getEnd()](#getEnd) | Gets the node that represents the field end. |
| [getErrorCorrectionLevel()](#getErrorCorrectionLevel) | Gets an error correction level of QR Code. |
| [getFieldCode()](#getFieldCode) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFixCheckDigit()](#getFixCheckDigit) | Gets whether to fix the check digit if it\\u2019s invalid. |
| [getForegroundColor()](#getForegroundColor) | Gets the foreground color of the barcode symbol. |
| [getFormat()](#getFormat) | Gets a [FieldFormat](../../com.aspose.words/fieldformat/) object that provides typed access to field's formatting. |
| [getLocaleId()](#getLocaleId) | Gets the LCID of the field. |
| [getPosCodeStyle()](#getPosCodeStyle) | Gets the style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). |
| [getResult()](#getResult) | Gets text that is between the field separator and field end. |
| [getScalingFactor()](#getScalingFactor) | Gets a scaling factor for the symbol. |
| [getSeparator()](#getSeparator) | Gets the node that represents the field separator. |
| [getStart()](#getStart) | Gets the node that represents the start of the field. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getSymbolHeight()](#getSymbolHeight) | Gets the height of the symbol. |
| [getSymbolRotation()](#getSymbolRotation) | Gets the rotation of the barcode symbol. |
| [getType()](#getType) | Gets the Microsoft Word field type. |
| [hashCode()](#hashCode) |  |
| [isDirty()](#isDirty) | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isDirty(boolean value)](#isDirty-boolean) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isLocked()](#isLocked) | Gets whether the field is locked (should not recalculate its result). |
| [isLocked(boolean value)](#isLocked-boolean) | Sets whether the field is locked (should not recalculate its result). |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [remove()](#remove) | Removes the field from the document. |
| [setAddStartStopChar(boolean value)](#setAddStartStopChar-boolean) | Sets whether to add Start/Stop characters for barcode types NW7 and CODE39. |
| [setBackgroundColor(String value)](#setBackgroundColor-java.lang.String) | Sets the background color of the barcode symbol. |
| [setBarcodeType(String value)](#setBarcodeType-java.lang.String) | Sets the barcode type (QR, etc.) |
| [setBarcodeValue(String value)](#setBarcodeValue-java.lang.String) | Sets the barcode value. |
| [setCaseCodeStyle(String value)](#setCaseCodeStyle-java.lang.String) | Sets the style of a Case Code for barcode type ITF14. |
| [setDisplayText(boolean value)](#setDisplayText-boolean) | Sets whether to display barcode data (text) along with image. |
| [setErrorCorrectionLevel(String value)](#setErrorCorrectionLevel-java.lang.String) | Sets an error correction level of QR Code. |
| [setFixCheckDigit(boolean value)](#setFixCheckDigit-boolean) | Sets whether to fix the check digit if it\\u2019s invalid. |
| [setForegroundColor(String value)](#setForegroundColor-java.lang.String) | Sets the foreground color of the barcode symbol. |
| [setLocaleId(int value)](#setLocaleId-int) | Sets the LCID of the field. |
| [setPosCodeStyle(String value)](#setPosCodeStyle-java.lang.String) | Sets the style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). |
| [setResult(String value)](#setResult-java.lang.String) | Sets text that is between the field separator and field end. |
| [setScalingFactor(String value)](#setScalingFactor-java.lang.String) | Sets a scaling factor for the symbol. |
| [setSymbolHeight(String value)](#setSymbolHeight-java.lang.String) | Sets the height of the symbol. |
| [setSymbolRotation(String value)](#setSymbolRotation-java.lang.String) | Sets the rotation of the barcode symbol. |
| [toString()](#toString) |  |
| [unlink()](#unlink) | Performs the field unlink. |
| [update()](#update) | Performs the field update. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | Performs a field update. |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getAddStartStopChar() {#getAddStartStopChar}
```
public boolean getAddStartStopChar()
```


Gets whether to add Start/Stop characters for barcode types NW7 and CODE39.

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Returns:**
boolean - Whether to add Start/Stop characters for barcode types NW7 and CODE39.
### getBackgroundColor() {#getBackgroundColor}
```
public String getBackgroundColor()
```


Gets the background color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF]

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Returns:**
java.lang.String - The background color of the barcode symbol.
### getBarcodeType() {#getBarcodeType}
```
public String getBarcodeType()
```


Gets the barcode type (QR, etc.)

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Returns:**
java.lang.String - The barcode type (QR, etc.)
### getBarcodeValue() {#getBarcodeValue}
```
public String getBarcodeValue()
```


Gets the barcode value.

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Returns:**
java.lang.String - The barcode value.
### getCaseCodeStyle() {#getCaseCodeStyle}
```
public String getCaseCodeStyle()
```


Gets the style of a Case Code for barcode type ITF14. The valid values are [STD|EXT|ADD]

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Returns:**
java.lang.String - The style of a Case Code for barcode type ITF14.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getDisplayResult() {#getDisplayResult}
```
public String getDisplayResult()
```


Gets the text that represents the displayed field result.

 **Remarks:** 

The [Document.updateListLabels()](../../com.aspose.words/document/\#updateListLabels) method must be called to obtain correct value for the [FieldListNum](../../com.aspose.words/fieldlistnum/), [FieldAutoNum](../../com.aspose.words/fieldautonum/), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout/) and [FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl/) fields.

 **Examples:** 

Shows how to get the real text that a field displays in the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("This document was written by ");
 FieldAuthor fieldAuthor = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);
 fieldAuthor.setAuthorName("John Doe");

 // We can use the DisplayResult property to verify what exact text
 // a field would display in its place in the document.
 Assert.assertEquals("", fieldAuthor.getDisplayResult());

 // Fields do not maintain accurate result values in real-time.
 // To make sure our fields display accurate results at any given time,
 // such as right before a save operation, we need to update them manually.
 fieldAuthor.update();

 Assert.assertEquals("John Doe", fieldAuthor.getDisplayResult());

 doc.save(getArtifactsDir() + "Field.DisplayResult.docx");
 
```

**Returns:**
java.lang.String - The text that represents the displayed field result.
### getDisplayText() {#getDisplayText}
```
public boolean getDisplayText()
```


Gets whether to display barcode data (text) along with image.

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Returns:**
boolean - Whether to display barcode data (text) along with image.
### getEnd() {#getEnd}
```
public FieldEnd getEnd()
```


Gets the node that represents the field end.

 **Examples:** 

Shows how to work with a collection of fields.

```

 public void fieldCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");
     doc.updateFields();

     FieldCollection fields = doc.getRange().getFields();

     Assert.assertEquals(6, fields.getCount());

     // Iterate over the field collection, and print contents and type
     // of every field using a custom visitor implementation.
     FieldVisitor fieldVisitor = new FieldVisitor();

     Iterator fieldEnumerator = fields.iterator();

     while (fieldEnumerator.hasNext()) {
         if (fieldEnumerator != null) {
             Field currentField = fieldEnumerator.next();

             currentField.getStart().accept(fieldVisitor);
             if (currentField.getSeparator() != null) {
                 currentField.getSeparator().accept(fieldVisitor);
             }
             currentField.getEnd().accept(fieldVisitor);
         } else {
             System.out.println("There are no fields in the document.");
         }
     }

     System.out.println(fieldVisitor.getText());
 }

 /// 
 /// Document visitor implementation that prints field info.
 /// 
 public static class FieldVisitor extends DocumentVisitor {
     public FieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         mBuilder.append("Found field: " + fieldStart.getFieldType() + "\r\n");
         mBuilder.append("\tField code: " + fieldStart.getField().getFieldCode() + "\r\n");
         mBuilder.append("\tDisplayed as: " + fieldStart.getField().getResult() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         mBuilder.append("\tFound separator: " + fieldSeparator.getText() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mBuilder.append("End of field: " + fieldEnd.getFieldType() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final  StringBuilder mBuilder;
 }
 
```

**Returns:**
[FieldEnd](../../com.aspose.words/fieldend/) - The node that represents the field end.
### getErrorCorrectionLevel() {#getErrorCorrectionLevel}
```
public String getErrorCorrectionLevel()
```


Gets an error correction level of QR Code. Valid values are [0, 3].

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Returns:**
java.lang.String - An error correction level of QR Code.
### getFieldCode() {#getFieldCode}
```
public String getFieldCode()
```


Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.

 **Examples:** 

Shows how to insert a field into a document using a field code.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

Shows how to get a field's field code.

```

 // Open a document which contains a MERGEFIELD inside an IF field.
 Document doc = new Document(getMyDir() + "Nested fields.docx");
 FieldIf fieldIf = (FieldIf) doc.getRange().getFields().get(0);

 // There are two ways of getting a field's field code:
 // 1 -  Omit its inner fields:
 Assert.assertEquals(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.getFieldCode(false));

 // 2 -  Include its inner fields:
 Assert.assertEquals(" IF  MERGEFIELD NetIncome  > 0 \" (surplus of  MERGEFIELD  NetIncome \\f $ ) \" \"\" ",
         fieldIf.getFieldCode(true));

 // By default, the GetFieldCode method displays inner fields.
 Assert.assertEquals(fieldIf.getFieldCode(), fieldIf.getFieldCode(true));
 
```

**Returns:**
java.lang.String
### getFieldCode(boolean includeChildFieldCodes) {#getFieldCode-boolean}
```
public String getFieldCode(boolean includeChildFieldCodes)
```


Returns text between field start and field separator (or field end if there is no separator).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| includeChildFieldCodes | boolean |  true  if child field codes should be included.

 **Examples:** 

Shows how to get a field's field code.

```

 // Open a document which contains a MERGEFIELD inside an IF field.
 Document doc = new Document(getMyDir() + "Nested fields.docx");
 FieldIf fieldIf = (FieldIf) doc.getRange().getFields().get(0);

 // There are two ways of getting a field's field code:
 // 1 -  Omit its inner fields:
 Assert.assertEquals(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.getFieldCode(false));

 // 2 -  Include its inner fields:
 Assert.assertEquals(" IF  MERGEFIELD NetIncome  > 0 \" (surplus of  MERGEFIELD  NetIncome \\f $ ) \" \"\" ",
         fieldIf.getFieldCode(true));

 // By default, the GetFieldCode method displays inner fields.
 Assert.assertEquals(fieldIf.getFieldCode(), fieldIf.getFieldCode(true));
 
``` |

**Returns:**
java.lang.String
### getFixCheckDigit() {#getFixCheckDigit}
```
public boolean getFixCheckDigit()
```


Gets whether to fix the check digit if it\\u2019s invalid.

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Returns:**
boolean - Whether to fix the check digit if it\\u2019s invalid.
### getForegroundColor() {#getForegroundColor}
```
public String getForegroundColor()
```


Gets the foreground color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF]

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Returns:**
java.lang.String - The foreground color of the barcode symbol.
### getFormat() {#getFormat}
```
public FieldFormat getFormat()
```


Gets a [FieldFormat](../../com.aspose.words/fieldformat/) object that provides typed access to field's formatting.

 **Examples:** 

Shows how to format field results.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use a document builder to insert a field that displays a result with no format applied.
 Field field = builder.insertField("= 2 + 3");

 Assert.assertEquals("= 2 + 3", field.getFieldCode());
 Assert.assertEquals("5", field.getResult());

 // We can apply a format to a field's result using the field's properties.
 // Below are three types of formats that we can apply to a field's result.
 // 1 -  Numeric format:
 FieldFormat format = field.getFormat();
 format.setNumericFormat("$###.00");
 field.update();

 Assert.assertEquals("= 2 + 3 \\# $###.00", field.getFieldCode());
 Assert.assertEquals("$  5.00", field.getResult());

 // 2 -  Date/time format:
 field = builder.insertField("DATE");
 format = field.getFormat();
 format.setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 Assert.assertEquals("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());
 System.out.println("Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

 // 3 -  General format:
 field = builder.insertField("= 25 + 33");
 format = field.getFormat();
 format.getGeneralFormats().add(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().add(GeneralFormat.UPPER);
 field.update();

 int index = 0;
 Iterator generalFormatEnumerator = format.getGeneralFormats().iterator();
 while (generalFormatEnumerator.hasNext()) {
     int value = generalFormatEnumerator.next();
     System.out.println(MessageFormat.format("General format index {0}: {1}", index++, value));
 }

 Assert.assertEquals("= 25 + 33 \\* roman \\* Upper", field.getFieldCode());
 Assert.assertEquals("LVIII", field.getResult());
 Assert.assertEquals(2, format.getGeneralFormats().getCount());
 Assert.assertEquals(GeneralFormat.LOWERCASE_ROMAN, format.getGeneralFormats().get(0));

 // We can remove our formats to revert the field's result to its original form.
 format.getGeneralFormats().remove(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().removeAt(0);
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 field.update();

 Assert.assertEquals("= 25 + 33  ", field.getFieldCode());
 Assert.assertEquals("58", field.getResult());
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 
```

**Returns:**
[FieldFormat](../../com.aspose.words/fieldformat/) - A [FieldFormat](../../com.aspose.words/fieldformat/) object that provides typed access to field's formatting.
### getLocaleId() {#getLocaleId}
```
public int getLocaleId()
```


Gets the LCID of the field.

 **Examples:** 

Shows how to insert a field and work with its locale.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a DATE field, and then print the date it will display.
 // Your thread's current culture determines the formatting of the date.
 Field field = builder.insertField("DATE");
 System.out.println(MessageFormat.format("Today''s date, as displayed in the \"{0}\" culture: {1}", Locale.getDefault().getDisplayLanguage(), field.getResult()));

 Assert.assertEquals(1033, field.getLocaleId());
 // Changing the culture of our thread will impact the result of the DATE field.
 // Another way to get the DATE field to display a date in a different culture is to use its LocaleId property.
 // This way allows us to avoid changing the thread's culture to get this effect.
 doc.getFieldOptions().setFieldUpdateCultureSource(FieldUpdateCultureSource.FIELD_CODE);
 CultureInfo de = new CultureInfo("de-DE");
 field.setLocaleId(1031);
 field.update();

 System.out.println(MessageFormat.format("Today''s date, as displayed according to the \"{0}\" culture: {1}", Locale.forLanguageTag(LocaleUtil.getLocaleFromLCID(field.getLocaleId())).getDisplayLanguage(), field.getResult()));
 
```

**Returns:**
int - The LCID of the field.
### getPosCodeStyle() {#getPosCodeStyle}
```
public String getPosCodeStyle()
```


Gets the style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). The valid values (case insensitive) are [STD|SUP2|SUP5|CASE].

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Returns:**
java.lang.String - The style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8).
### getResult() {#getResult}
```
public String getResult()
```


Gets text that is between the field separator and field end.

 **Examples:** 

Shows how to insert a field into a document using a field code.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
java.lang.String - Text that is between the field separator and field end.
### getScalingFactor() {#getScalingFactor}
```
public String getScalingFactor()
```


Gets a scaling factor for the symbol. The value is in whole percentage points and the valid values are [10, 1000]

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Returns:**
java.lang.String - A scaling factor for the symbol.
### getSeparator() {#getSeparator}
```
public FieldSeparator getSeparator()
```


Gets the node that represents the field separator. Can be  null .

 **Examples:** 

Shows how to work with a collection of fields.

```

 public void fieldCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");
     doc.updateFields();

     FieldCollection fields = doc.getRange().getFields();

     Assert.assertEquals(6, fields.getCount());

     // Iterate over the field collection, and print contents and type
     // of every field using a custom visitor implementation.
     FieldVisitor fieldVisitor = new FieldVisitor();

     Iterator fieldEnumerator = fields.iterator();

     while (fieldEnumerator.hasNext()) {
         if (fieldEnumerator != null) {
             Field currentField = fieldEnumerator.next();

             currentField.getStart().accept(fieldVisitor);
             if (currentField.getSeparator() != null) {
                 currentField.getSeparator().accept(fieldVisitor);
             }
             currentField.getEnd().accept(fieldVisitor);
         } else {
             System.out.println("There are no fields in the document.");
         }
     }

     System.out.println(fieldVisitor.getText());
 }

 /// 
 /// Document visitor implementation that prints field info.
 /// 
 public static class FieldVisitor extends DocumentVisitor {
     public FieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         mBuilder.append("Found field: " + fieldStart.getFieldType() + "\r\n");
         mBuilder.append("\tField code: " + fieldStart.getField().getFieldCode() + "\r\n");
         mBuilder.append("\tDisplayed as: " + fieldStart.getField().getResult() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         mBuilder.append("\tFound separator: " + fieldSeparator.getText() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mBuilder.append("End of field: " + fieldEnd.getFieldType() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final  StringBuilder mBuilder;
 }
 
```

**Returns:**
[FieldSeparator](../../com.aspose.words/fieldseparator/) - The node that represents the field separator.
### getStart() {#getStart}
```
public FieldStart getStart()
```


Gets the node that represents the start of the field.

 **Examples:** 

Shows how to work with a collection of fields.

```

 public void fieldCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");
     doc.updateFields();

     FieldCollection fields = doc.getRange().getFields();

     Assert.assertEquals(6, fields.getCount());

     // Iterate over the field collection, and print contents and type
     // of every field using a custom visitor implementation.
     FieldVisitor fieldVisitor = new FieldVisitor();

     Iterator fieldEnumerator = fields.iterator();

     while (fieldEnumerator.hasNext()) {
         if (fieldEnumerator != null) {
             Field currentField = fieldEnumerator.next();

             currentField.getStart().accept(fieldVisitor);
             if (currentField.getSeparator() != null) {
                 currentField.getSeparator().accept(fieldVisitor);
             }
             currentField.getEnd().accept(fieldVisitor);
         } else {
             System.out.println("There are no fields in the document.");
         }
     }

     System.out.println(fieldVisitor.getText());
 }

 /// 
 /// Document visitor implementation that prints field info.
 /// 
 public static class FieldVisitor extends DocumentVisitor {
     public FieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         mBuilder.append("Found field: " + fieldStart.getFieldType() + "\r\n");
         mBuilder.append("\tField code: " + fieldStart.getField().getFieldCode() + "\r\n");
         mBuilder.append("\tDisplayed as: " + fieldStart.getField().getResult() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         mBuilder.append("\tFound separator: " + fieldSeparator.getText() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mBuilder.append("End of field: " + fieldEnd.getFieldType() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final  StringBuilder mBuilder;
 }
 
```

**Returns:**
[FieldStart](../../com.aspose.words/fieldstart/) - The node that represents the start of the field.
### getSwitchType(String switchName) {#getSwitchType-java.lang.String}
```
public int getSwitchType(String switchName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Returns:**
int
### getSymbolHeight() {#getSymbolHeight}
```
public String getSymbolHeight()
```


Gets the height of the symbol. The units are in TWIPS (1/1440 inch).

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Returns:**
java.lang.String - The height of the symbol.
### getSymbolRotation() {#getSymbolRotation}
```
public String getSymbolRotation()
```


Gets the rotation of the barcode symbol. Valid values are [0, 3]

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Returns:**
java.lang.String - The rotation of the barcode symbol.
### getType() {#getType}
```
public int getType()
```


Gets the Microsoft Word field type.

 **Examples:** 

Shows how to insert a field into a document using a field code.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
int - The Microsoft Word field type. The returned value is one of [FieldType](../../com.aspose.words/fieldtype/) constants.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isDirty() {#isDirty}
```
public boolean isDirty()
```


Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.

 **Examples:** 

Shows how to use special property for updating field result.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Give the document's built-in "Author" property value, and then display it with a field.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 FieldAuthor field = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);

 Assert.assertFalse(field.isDirty());
 Assert.assertEquals("John Doe", field.getResult());

 // Update the property. The field still displays the old value.
 doc.getBuiltInDocumentProperties().setAuthor("John & Jane Doe");

 Assert.assertEquals("John Doe", field.getResult());

 // Since the field's value is out of date, we can mark it as "dirty".
 // This value will stay out of date until we update the field manually with the Field.Update() method.
 field.isDirty(true);

 // If we save without calling an update method,
 // the field will keep displaying the out of date value in the output document.
 doc.save(getArtifactsDir() + "Filed.UpdateDirtyFields.docx");

 // The LoadOptions object has an option to update all fields
 // marked as "dirty" when loading the document.
 LoadOptions options = new LoadOptions();
 options.setUpdateDirtyFields(updateDirtyFields);

 doc = new Document(getArtifactsDir() + "Filed.UpdateDirtyFields.docx", options);

 Assert.assertEquals("John & Jane Doe", doc.getBuiltInDocumentProperties().getAuthor());

 field = (FieldAuthor) doc.getRange().getFields().get(0);

 // Updating dirty fields like this automatically set their "IsDirty" flag to false.
 if (updateDirtyFields) {
     Assert.assertEquals("John & Jane Doe", field.getResult());
     Assert.assertFalse(field.isDirty());
 } else {
     Assert.assertEquals("John Doe", field.getResult());
     Assert.assertTrue(field.isDirty());
 }
 
```

**Returns:**
boolean - Whether the current result of the field is no longer correct (stale) due to other modifications made to the document.
### isDirty(boolean value) {#isDirty-boolean}
```
public void isDirty(boolean value)
```


Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.

 **Examples:** 

Shows how to use special property for updating field result.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Give the document's built-in "Author" property value, and then display it with a field.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 FieldAuthor field = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);

 Assert.assertFalse(field.isDirty());
 Assert.assertEquals("John Doe", field.getResult());

 // Update the property. The field still displays the old value.
 doc.getBuiltInDocumentProperties().setAuthor("John & Jane Doe");

 Assert.assertEquals("John Doe", field.getResult());

 // Since the field's value is out of date, we can mark it as "dirty".
 // This value will stay out of date until we update the field manually with the Field.Update() method.
 field.isDirty(true);

 // If we save without calling an update method,
 // the field will keep displaying the out of date value in the output document.
 doc.save(getArtifactsDir() + "Filed.UpdateDirtyFields.docx");

 // The LoadOptions object has an option to update all fields
 // marked as "dirty" when loading the document.
 LoadOptions options = new LoadOptions();
 options.setUpdateDirtyFields(updateDirtyFields);

 doc = new Document(getArtifactsDir() + "Filed.UpdateDirtyFields.docx", options);

 Assert.assertEquals("John & Jane Doe", doc.getBuiltInDocumentProperties().getAuthor());

 field = (FieldAuthor) doc.getRange().getFields().get(0);

 // Updating dirty fields like this automatically set their "IsDirty" flag to false.
 if (updateDirtyFields) {
     Assert.assertEquals("John & Jane Doe", field.getResult());
     Assert.assertFalse(field.isDirty());
 } else {
     Assert.assertEquals("John Doe", field.getResult());
     Assert.assertTrue(field.isDirty());
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |

### isLocked() {#isLocked}
```
public boolean isLocked()
```


Gets whether the field is locked (should not recalculate its result).

 **Examples:** 

Shows how to work with a FieldStart node.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDate field = (FieldDate) builder.insertField(FieldType.FIELD_DATE, true);
 field.getFormat().setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 FieldChar fieldStart = field.getStart();

 Assert.assertEquals(FieldType.FIELD_DATE, fieldStart.getFieldType());
 Assert.assertEquals(false, fieldStart.isDirty());
 Assert.assertEquals(false, fieldStart.isLocked());

 // Retrieve the facade object which represents the field in the document.
 field = (FieldDate) fieldStart.getField();

 Assert.assertEquals(false, field.isLocked());
 Assert.assertEquals(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());

 // Update the field to show the current date.
 field.update();
 
```

**Returns:**
boolean - Whether the field is locked (should not recalculate its result).
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


Sets whether the field is locked (should not recalculate its result).

 **Examples:** 

Shows how to work with a FieldStart node.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDate field = (FieldDate) builder.insertField(FieldType.FIELD_DATE, true);
 field.getFormat().setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 FieldChar fieldStart = field.getStart();

 Assert.assertEquals(FieldType.FIELD_DATE, fieldStart.getFieldType());
 Assert.assertEquals(false, fieldStart.isDirty());
 Assert.assertEquals(false, fieldStart.isLocked());

 // Retrieve the facade object which represents the field in the document.
 field = (FieldDate) fieldStart.getField();

 Assert.assertEquals(false, field.isLocked());
 Assert.assertEquals(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());

 // Update the field to show the current date.
 field.update();
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the field is locked (should not recalculate its result). |

### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### remove() {#remove}
```
public Node remove()
```


Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns  null .

 **Examples:** 

Shows how to remove fields from a field collection.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
 builder.insertField(" TIME ");
 builder.insertField(" REVNUM ");
 builder.insertField(" AUTHOR  \"John Doe\" ");
 builder.insertField(" SUBJECT \"My Subject\" ");
 builder.insertField(" QUOTE \"Hello world!\" ");
 doc.updateFields();

 FieldCollection fields = doc.getRange().getFields();

 Assert.assertEquals(6, fields.getCount());

 // Below are four ways of removing fields from a field collection.
 // 1 -  Get a field to remove itself:
 fields.get(0).remove();
 Assert.assertEquals(5, fields.getCount());

 // 2 -  Get the collection to remove a field that we pass to its removal method:
 Field lastField = fields.get(3);
 fields.remove(lastField);
 Assert.assertEquals(4, fields.getCount());

 // 3 -  Remove a field from a collection at an index:
 fields.removeAt(2);
 Assert.assertEquals(3, fields.getCount());

 // 4 -  Remove all the fields from the collection at once:
 fields.clear();
 Assert.assertEquals(0, fields.getCount());
 
```

Shows how to process PRIVATE fields.

```

 public void fieldPrivate() throws Exception {
     // Open a Corel WordPerfect document which we have converted to .docx format.
     Document doc = new Document(getMyDir() + "Field sample - PRIVATE.docx");

     // WordPerfect 5.x/6.x documents like the one we have loaded may contain PRIVATE fields.
     // Microsoft Word preserves PRIVATE fields during load/save operations,
     // but provides no functionality for them.
     FieldPrivate field = (FieldPrivate) doc.getRange().getFields().get(0);

     Assert.assertEquals(" PRIVATE \"My value\" ", field.getFieldCode());
     Assert.assertEquals(FieldType.FIELD_PRIVATE, field.getType());

     // We can also insert PRIVATE fields using a document builder.
     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.insertField(FieldType.FIELD_PRIVATE, true);

     // These fields are not a viable way of protecting sensitive information.
     // Unless backward compatibility with older versions of WordPerfect is essential,
     // we can safely remove these fields. We can do this using a DocumentVisiitor implementation.
     Assert.assertEquals(2, doc.getRange().getFields().getCount());

     FieldPrivateRemover remover = new FieldPrivateRemover();
     doc.accept(remover);

     Assert.assertEquals(remover.getFieldsRemovedCount(), 2);
     Assert.assertEquals(doc.getRange().getFields().getCount(), 0);
 }

 /// 
 /// Removes all encountered PRIVATE fields.
 /// 
 public static class FieldPrivateRemover extends DocumentVisitor {
     public FieldPrivateRemover() {
         mFieldsRemovedCount = 0;
     }

     public int getFieldsRemovedCount() {
         return mFieldsRemovedCount;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// If the node belongs to a PRIVATE field, the entire field is removed.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) throws Exception {
         if (fieldEnd.getFieldType() == FieldType.FIELD_PRIVATE) {
             fieldEnd.getField().remove();
             mFieldsRemovedCount++;
         }

         return VisitorAction.CONTINUE;
     }

     private int mFieldsRemovedCount;
 }
 
```

**Returns:**
[Node](../../com.aspose.words/node/)
### setAddStartStopChar(boolean value) {#setAddStartStopChar-boolean}
```
public void setAddStartStopChar(boolean value)
```


Sets whether to add Start/Stop characters for barcode types NW7 and CODE39.

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to add Start/Stop characters for barcode types NW7 and CODE39. |

### setBackgroundColor(String value) {#setBackgroundColor-java.lang.String}
```
public void setBackgroundColor(String value)
```


Sets the background color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF]

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The background color of the barcode symbol. |

### setBarcodeType(String value) {#setBarcodeType-java.lang.String}
```
public void setBarcodeType(String value)
```


Sets the barcode type (QR, etc.)

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The barcode type (QR, etc.) |

### setBarcodeValue(String value) {#setBarcodeValue-java.lang.String}
```
public void setBarcodeValue(String value)
```


Sets the barcode value.

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The barcode value. |

### setCaseCodeStyle(String value) {#setCaseCodeStyle-java.lang.String}
```
public void setCaseCodeStyle(String value)
```


Sets the style of a Case Code for barcode type ITF14. The valid values are [STD|EXT|ADD]

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The style of a Case Code for barcode type ITF14. |

### setDisplayText(boolean value) {#setDisplayText-boolean}
```
public void setDisplayText(boolean value)
```


Sets whether to display barcode data (text) along with image.

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to display barcode data (text) along with image. |

### setErrorCorrectionLevel(String value) {#setErrorCorrectionLevel-java.lang.String}
```
public void setErrorCorrectionLevel(String value)
```


Sets an error correction level of QR Code. Valid values are [0, 3].

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | An error correction level of QR Code. |

### setFixCheckDigit(boolean value) {#setFixCheckDigit-boolean}
```
public void setFixCheckDigit(boolean value)
```


Sets whether to fix the check digit if it\\u2019s invalid.

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to fix the check digit if it\\u2019s invalid. |

### setForegroundColor(String value) {#setForegroundColor-java.lang.String}
```
public void setForegroundColor(String value)
```


Sets the foreground color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF]

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The foreground color of the barcode symbol. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Sets the LCID of the field.

 **Examples:** 

Shows how to insert a field and work with its locale.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a DATE field, and then print the date it will display.
 // Your thread's current culture determines the formatting of the date.
 Field field = builder.insertField("DATE");
 System.out.println(MessageFormat.format("Today''s date, as displayed in the \"{0}\" culture: {1}", Locale.getDefault().getDisplayLanguage(), field.getResult()));

 Assert.assertEquals(1033, field.getLocaleId());
 // Changing the culture of our thread will impact the result of the DATE field.
 // Another way to get the DATE field to display a date in a different culture is to use its LocaleId property.
 // This way allows us to avoid changing the thread's culture to get this effect.
 doc.getFieldOptions().setFieldUpdateCultureSource(FieldUpdateCultureSource.FIELD_CODE);
 CultureInfo de = new CultureInfo("de-DE");
 field.setLocaleId(1031);
 field.update();

 System.out.println(MessageFormat.format("Today''s date, as displayed according to the \"{0}\" culture: {1}", Locale.forLanguageTag(LocaleUtil.getLocaleFromLCID(field.getLocaleId())).getDisplayLanguage(), field.getResult()));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The LCID of the field. |

### setPosCodeStyle(String value) {#setPosCodeStyle-java.lang.String}
```
public void setPosCodeStyle(String value)
```


Sets the style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). The valid values (case insensitive) are [STD|SUP2|SUP5|CASE].

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). |

### setResult(String value) {#setResult-java.lang.String}
```
public void setResult(String value)
```


Sets text that is between the field separator and field end.

 **Examples:** 

Shows how to insert a field into a document using a field code.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Text that is between the field separator and field end. |

### setScalingFactor(String value) {#setScalingFactor-java.lang.String}
```
public void setScalingFactor(String value)
```


Sets a scaling factor for the symbol. The value is in whole percentage points and the valid values are [10, 1000]

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A scaling factor for the symbol. |

### setSymbolHeight(String value) {#setSymbolHeight-java.lang.String}
```
public void setSymbolHeight(String value)
```


Sets the height of the symbol. The units are in TWIPS (1/1440 inch).

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The height of the symbol. |

### setSymbolRotation(String value) {#setSymbolRotation-java.lang.String}
```
public void setSymbolRotation(String value)
```


Sets the rotation of the barcode symbol. Valid values are [0, 3]

 **Examples:** 

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDisplayBarcode field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);

 // Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
 // 1 -  QR code with custom colors:
 field.setBarcodeType("QR");
 field.setBarcodeValue("ABC123");
 field.setBackgroundColor("0xF8BD69");
 field.setForegroundColor("0xB5413B");
 field.setErrorCorrectionLevel("3");
 field.setScalingFactor("250");
 field.setSymbolHeight("1000");
 field.setSymbolRotation("0");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0");
 builder.writeln();

 // 2 -  EAN13 barcode, with the digits displayed below the bars:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("501234567890");
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x");
 builder.writeln();

 // 3 -  CODE39 barcode:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("12345ABCDE");
 field.setAddStartStopChar(true);

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  12345ABCDE CODE39 \\d");
 builder.writeln();

 // 4 -  ITF4 barcode, with a specified case code:
 field = (FieldDisplayBarcode) builder.insertField(FieldType.FIELD_DISPLAY_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("09312345678907");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(field.getFieldCode(), " DISPLAYBARCODE  09312345678907 ITF14 \\c STD");

 doc.save(getArtifactsDir() + "Field.DISPLAYBARCODE.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The rotation of the barcode symbol. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### unlink() {#unlink}
```
public boolean unlink()
```


Performs the field unlink.

 **Remarks:** 

Replaces the field with its most recent result.

Some fields, such as XE (Index Entry) fields and SEQ (Sequence) fields, cannot be unlinked.

**Returns:**
boolean -  true  if the field has been unlinked, otherwise  false .

 **Examples:** 

Shows how to unlink a field.

```

 Document doc = new Document(getMyDir() + "Linked fields.docx");
 doc.getRange().getFields().get(1).unlink();
 
```
### update() {#update}
```
public void update()
```


Performs the field update. Throws if the field is being updated already.

 **Examples:** 

Shows how to insert a field into a document using FieldType.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert two fields while passing a flag which determines whether to update them as the builder inserts them.
 // In some cases, updating fields could be computationally expensive, and it may be a good idea to defer the update.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 builder.write("This document was written by ");
 builder.insertField(FieldType.FIELD_AUTHOR, updateInsertedFieldsImmediately);

 builder.insertParagraph();
 builder.write("\nThis is page ");
 builder.insertField(FieldType.FIELD_PAGE, updateInsertedFieldsImmediately);

 Assert.assertEquals(" AUTHOR ", doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(" PAGE ", doc.getRange().getFields().get(1).getFieldCode());

 if (updateInsertedFieldsImmediately) {
     Assert.assertEquals("John Doe", doc.getRange().getFields().get(0).getResult());
     Assert.assertEquals("1", doc.getRange().getFields().get(1).getResult());
 } else {
     Assert.assertEquals("", doc.getRange().getFields().get(0).getResult());
     Assert.assertEquals("", doc.getRange().getFields().get(1).getResult());

     // We will need to update these fields using the update methods manually.
     doc.getRange().getFields().get(0).update();

     Assert.assertEquals("John Doe", doc.getRange().getFields().get(0).getResult());

     doc.updateFields();

     Assert.assertEquals("1", doc.getRange().getFields().get(1).getResult());
 }
 
```

Shows how to format field results.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use a document builder to insert a field that displays a result with no format applied.
 Field field = builder.insertField("= 2 + 3");

 Assert.assertEquals("= 2 + 3", field.getFieldCode());
 Assert.assertEquals("5", field.getResult());

 // We can apply a format to a field's result using the field's properties.
 // Below are three types of formats that we can apply to a field's result.
 // 1 -  Numeric format:
 FieldFormat format = field.getFormat();
 format.setNumericFormat("$###.00");
 field.update();

 Assert.assertEquals("= 2 + 3 \\# $###.00", field.getFieldCode());
 Assert.assertEquals("$  5.00", field.getResult());

 // 2 -  Date/time format:
 field = builder.insertField("DATE");
 format = field.getFormat();
 format.setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 Assert.assertEquals("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());
 System.out.println("Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

 // 3 -  General format:
 field = builder.insertField("= 25 + 33");
 format = field.getFormat();
 format.getGeneralFormats().add(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().add(GeneralFormat.UPPER);
 field.update();

 int index = 0;
 Iterator generalFormatEnumerator = format.getGeneralFormats().iterator();
 while (generalFormatEnumerator.hasNext()) {
     int value = generalFormatEnumerator.next();
     System.out.println(MessageFormat.format("General format index {0}: {1}", index++, value));
 }

 Assert.assertEquals("= 25 + 33 \\* roman \\* Upper", field.getFieldCode());
 Assert.assertEquals("LVIII", field.getResult());
 Assert.assertEquals(2, format.getGeneralFormats().getCount());
 Assert.assertEquals(GeneralFormat.LOWERCASE_ROMAN, format.getGeneralFormats().get(0));

 // We can remove our formats to revert the field's result to its original form.
 format.getGeneralFormats().remove(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().removeAt(0);
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 field.update();

 Assert.assertEquals("= 25 + 33  ", field.getFieldCode());
 Assert.assertEquals("58", field.getResult());
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 
```

### update(boolean ignoreMergeFormat) {#update-boolean}
```
public void update(boolean ignoreMergeFormat)
```


Performs a field update. Throws if the field is being updated already.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ignoreMergeFormat | boolean | If  true  then direct field result formatting is abandoned, regardless of the MERGEFORMAT switch, otherwise normal update is performed.

 **Examples:** 

Shows how to preserve or discard INCLUDEPICTURE fields when loading a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldIncludePicture includePicture = (FieldIncludePicture) builder.insertField(FieldType.FIELD_INCLUDE_PICTURE, true);
 includePicture.setSourceFullName(getImageDir() + "Transparent background logo.png");
 includePicture.update(true);

 try (ByteArrayOutputStream docStream = new ByteArrayOutputStream()) {
     doc.save(docStream, new OoxmlSaveOptions(SaveFormat.DOCX));

     // We can set a flag in a LoadOptions object to decide whether to convert all INCLUDEPICTURE fields
     // into image shapes when loading a document that contains them.
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setPreserveIncludePictureField(preserveIncludePictureField);
     }

     doc = new Document(new ByteArrayInputStream(docStream.toByteArray()), loadOptions);
     FieldCollection fieldCollection = doc.getRange().getFields();

     if (preserveIncludePictureField) {
         Assert.assertTrue(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));

         doc.updateFields();
         doc.save(getArtifactsDir() + "Field.PreserveIncludePicture.docx");
     } else {
         Assert.assertFalse(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));
     }
 }
 
``` |

### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

