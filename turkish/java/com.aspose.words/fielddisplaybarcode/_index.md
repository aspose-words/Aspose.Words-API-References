---
title: "FieldDisplayBarcode"
linktitle: "FieldDisplayBarcode"
second_title: "Aspose.Words Java için"
description: "Java'da DISPLAYBARCODE alanını uygular."
type: docs
weight: 223
url: /tr/java/com.aspose.words/fielddisplaybarcode/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field/)
```
public class FieldDisplayBarcode extends Field
```

DISPLAYBARCODE alanını uygular.

Daha fazla bilgi için, [ Working with Fields ][Working with Fields] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Bir barkod ekler.

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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

QR barkodları üzerinde posta birleştirmenin nasıl yapılacağını gösterir.

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
 table.getRows().add("ABC123");
 table.getRows().add("DEF456");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  DEF456 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.QR.docx");
 
```


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getAddStartStopChar()](#getAddStartStopChar) | NW7 ve CODE39 barkod tipleri için Başlangıç/Bitiş karakterlerinin eklenip eklenmeyeceğini alır. |
| [getBackgroundColor()](#getBackgroundColor) | Barkod simgesinin arka plan rengini alır. |
| [getBarcodeType()](#getBarcodeType) | Barkod tipini (QR vb.) alır. |
| [getBarcodeValue()](#getBarcodeValue) | Barkod değerini alır. |
| [getCaseCodeStyle()](#getCaseCodeStyle) | ITF14 barkod tipi için Kasa Kodu stilini alır. |
| [getDisplayResult()](#getDisplayResult) | Görüntülenen alan sonucunu temsil eden metni alır. |
| [getDisplayText()](#getDisplayText) | Barkod verisinin (metin) görüntüyle birlikte gösterilip gösterilmeyeceğini alır. |
| [getEnd()](#getEnd) | Alan sonunu temsil eden düğümü alır. |
| [getErrorCorrectionLevel()](#getErrorCorrectionLevel) | QR Kodunun hata düzeltme seviyesini alır. |
| [getFieldCode()](#getFieldCode) | Alan başlangıcı ile alan ayırıcı arasındaki metni (veya ayırıcı yoksa alan sonunu) döndürür. |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Alan başlangıcı ile alan ayırıcı arasındaki metni (veya ayırıcı yoksa alan sonunu) döndürür. |
| [getFixCheckDigit()](#getFixCheckDigit) | Geçersiz olduğunda kontrol rakamını düzeltip düzeltmeyeceğini alır. |
| [getForegroundColor()](#getForegroundColor) | Barkod simgesinin ön plan rengini alır. |
| [getFormat()](#getFormat) | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../../com.aspose.words/fieldformat/) nesnesi alır. |
| [getLocaleId()](#getLocaleId) | Alanının LCID'sini alır. |
| [getPosCodeStyle()](#getPosCodeStyle) | Gets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). |
| [getResult()](#getResult) | Alan ayırıcı ile alan sonu arasındaki metni alır. |
| [getScalingFactor()](#getScalingFactor) | Sembol için bir ölçek faktörünü alır. |
| [getSeparator()](#getSeparator) | Alan ayırıcıyı temsil eden düğümü alır. |
| [getStart()](#getStart) | Alan başlangıcını temsil eden düğümü alır. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getSymbolHeight()](#getSymbolHeight) | Sembol yüksekliğini alır. |
| [getSymbolRotation()](#getSymbolRotation) | Barkod simgesinin dönüşünü alır. |
| [getType()](#getType) | Microsoft Word alan türünü alır. |
| [isDirty()](#isDirty) | Belgenin diğer değişiklikleri nedeniyle alanın mevcut sonucunun artık doğru (eski) olup olmadığını alır. |
| [isDirty(boolean value)](#isDirty-boolean) | Belgenin diğer değişiklikleri nedeniyle alanın mevcut sonucunun artık doğru (eski) olup olmadığını ayarlar. |
| [isLocked()](#isLocked) | Alan kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır. |
| [isLocked(boolean value)](#isLocked-boolean) | Alan kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) ayarlar. |
| [remove()](#remove) | Alanı belgeden kaldırır. |
| [setAddStartStopChar(boolean value)](#setAddStartStopChar-boolean) | NW7 ve CODE39 barkod tipleri için Başlangıç/Bitiş karakterlerinin eklenip eklenmeyeceğini ayarlar. |
| [setBackgroundColor(String value)](#setBackgroundColor-java.lang.String) | Barkod simgesinin arka plan rengini ayarlar. |
| [setBarcodeType(String value)](#setBarcodeType-java.lang.String) | Barkod tipini (QR vb.) ayarlar |
| [setBarcodeValue(String value)](#setBarcodeValue-java.lang.String) | Barkod değerini ayarlar. |
| [setCaseCodeStyle(String value)](#setCaseCodeStyle-java.lang.String) | ITF14 barkod tipi için Case Code stilini ayarlar. |
| [setDisplayText(boolean value)](#setDisplayText-boolean) | Barkod verisinin (metin) görüntüyle birlikte gösterilip gösterilmeyeceğini ayarlar. |
| [setErrorCorrectionLevel(String value)](#setErrorCorrectionLevel-java.lang.String) | QR Kodunun hata düzeltme seviyesini ayarlar. |
| [setFixCheckDigit(boolean value)](#setFixCheckDigit-boolean) | Geçersiz olduğunda kontrol basamağının düzeltilip düzeltilmeyeceğini ayarlar. |
| [setForegroundColor(String value)](#setForegroundColor-java.lang.String) | Barkod sembolünün ön plan rengini ayarlar. |
| [setLocaleId(int value)](#setLocaleId-int) | Alanının LCID'sini ayarlar. |
| [setPosCodeStyle(String value)](#setPosCodeStyle-java.lang.String) | Sets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). |
| [setResult(String value)](#setResult-java.lang.String) | Alan ayırıcı ile alan sonu arasındaki metni ayarlar. |
| [setScalingFactor(String value)](#setScalingFactor-java.lang.String) | Sembol için bir ölçek faktörü ayarlar. |
| [setSymbolHeight(String value)](#setSymbolHeight-java.lang.String) | Sembolün yüksekliğini ayarlar. |
| [setSymbolRotation(String value)](#setSymbolRotation-java.lang.String) | Barkod sembolünün dönüşünü ayarlar. |
| [unlink()](#unlink) | Alan bağlantısını kaldırır. |
| [update()](#update) | Alan güncellemesini gerçekleştirir. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | Bir alan güncellemesi gerçekleştirir. |
### getAddStartStopChar() {#getAddStartStopChar}
```
public boolean getAddStartStopChar()
```


NW7 ve CODE39 barkod tipleri için Başlangıç/Bitiş karakterlerinin eklenip eklenmeyeceğini alır.

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
boolean - NW7 ve CODE39 barkod tipleri için Başlangıç/Bitiş karakterlerinin eklenip eklenmeyeceği.
### getBackgroundColor() {#getBackgroundColor}
```
public String getBackgroundColor()
```


Barkod sembolünün arka plan rengini alır. Geçerli değerler [0, 0xFFFFFF] aralığındadır.

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
java.lang.String - Barkod sembolünün arka plan rengi.
### getBarcodeType() {#getBarcodeType}
```
public String getBarcodeType()
```


Barkod tipini (QR vb.) alır.

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
java.lang.String - Barkod tipi (QR vb.)
### getBarcodeValue() {#getBarcodeValue}
```
public String getBarcodeValue()
```


Barkod değerini alır.

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
java.lang.String - Barkod değeri.
### getCaseCodeStyle() {#getCaseCodeStyle}
```
public String getCaseCodeStyle()
```


ITF14 barkod tipi için Case Code stilini alır. Geçerli değerler [STD|EXT|ADD]

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
java.lang.String - ITF14 barkod tipi için Case Code stili.
### getDisplayResult() {#getDisplayResult}
```
public String getDisplayResult()
```


Görüntülenen alan sonucunu temsil eden metni alır.

 **Remarks:** 

Doğru değer elde etmek için [Document.updateListLabels()](../../com.aspose.words/document/\#updateListLabels) yöntemi, [FieldListNum](../../com.aspose.words/fieldlistnum/), [FieldAutoNum](../../com.aspose.words/fieldautonum/), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout/) ve [FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl/) alanları için çağrılmalıdır.

 **Examples:** 

Bir alanın belgede gösterdiği gerçek metni nasıl alacağınızı gösterir.

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
java.lang.String - Görüntülenen alan sonucunu temsil eden metin.
### getDisplayText() {#getDisplayText}
```
public boolean getDisplayText()
```


Barkod verisinin (metin) görüntüyle birlikte gösterilip gösterilmeyeceğini alır.

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
boolean - Barkod verisinin (metin) görüntüyle birlikte gösterilip gösterilmeyeceği.
### getEnd() {#getEnd}
```
public FieldEnd getEnd()
```


Alan sonunu temsil eden düğümü alır.

 **Examples:** 

Alan koleksiyonu ile nasıl çalışılacağını gösterir.

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


QR Kodunun hata düzeltme seviyesini alır. Geçerli değerler [0, 3].

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
java.lang.String - QR Kodunun hata düzeltme seviyesi.
### getFieldCode() {#getFieldCode}
```
public String getFieldCode()
```


Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların sonuçları dahil edilir.

 **Examples:** 

Alan kodu kullanarak bir alanı belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

Bir alanın alan kodunu nasıl alacağınızı gösterir.

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


Alan başlangıcı ile alan ayırıcı arasındaki metni (veya ayırıcı yoksa alan sonunu) döndürür.

 **Examples:** 

Bir alanın alan kodunu nasıl alacağınızı gösterir.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| includeChildFieldCodes | boolean | true  eğer alt alan kodları dahil edilmeliyse. |

**Returns:**
java.lang.String
### getFixCheckDigit() {#getFixCheckDigit}
```
public boolean getFixCheckDigit()
```


Geçersiz olduğunda kontrol rakamını düzeltip düzeltmeyeceğini alır.

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
boolean - Geçersiz olduğunda kontrol basamağının düzeltilip düzeltilmeyeceği.
### getForegroundColor() {#getForegroundColor}
```
public String getForegroundColor()
```


Barkod sembolünün ön plan rengini alır. Geçerli değerler [0, 0xFFFFFF] aralığındadır.

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
java.lang.String - Barkod sembolünün ön plan rengi.
### getFormat() {#getFormat}
```
public FieldFormat getFormat()
```


Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../../com.aspose.words/fieldformat/) nesnesi alır.

 **Examples:** 

Alan sonuçlarını nasıl biçimlendireceğinizi gösterir.

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


Alanının LCID'sini alır.

 **Examples:** 

Bir alanı nasıl ekleyeceğinizi ve yerel ayarıyla nasıl çalışacağınızı gösterir.

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
int - Alanın LCID'si.
### getPosCodeStyle() {#getPosCodeStyle}
```
public String getPosCodeStyle()
```


Satış noktası barkodu stilini (barkod tipleri UPCA|UPCE|EAN13|EAN8) alır. Geçerli değerler (büyük/küçük harfe duyarsız) [STD|SUP2|SUP5|CASE].

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
java.lang.String - Satış noktası barkodu stili (barkod tipleri UPCA|UPCE|EAN13|EAN8).
### getResult() {#getResult}
```
public String getResult()
```


Alan ayırıcı ile alan sonu arasındaki metni alır.

 **Examples:** 

Alan kodu kullanarak bir alanı belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
java.lang.String - Alan ayırıcı ile alan sonu arasındaki metin.
### getScalingFactor() {#getScalingFactor}
```
public String getScalingFactor()
```


Sembol için bir ölçekleme faktörü alır. Değer tam yüzde puanları cinsindendir ve geçerli değerler [10, 1000] aralığındadır.

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
java.lang.String - Sembol için bir ölçekleme faktörü.
### getSeparator() {#getSeparator}
```
public FieldSeparator getSeparator()
```


Alan ayırıcıyı temsil eden düğümü alır. Null olabilir.

 **Examples:** 

Alan koleksiyonu ile nasıl çalışılacağını gösterir.

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


Alan başlangıcını temsil eden düğümü alır.

 **Examples:** 

Alan koleksiyonu ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Returns:**
int
### getSymbolHeight() {#getSymbolHeight}
```
public String getSymbolHeight()
```


Sembol yüksekliğini alır. Birimler TWIPS cinsindendir (1/1440 inç).

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
java.lang.String - Sembol yüksekliği.
### getSymbolRotation() {#getSymbolRotation}
```
public String getSymbolRotation()
```


Barkod sembolünün dönüşünü alır. Geçerli değerler [0, 3]

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
java.lang.String - Barkod sembolünün dönüşü.
### getType() {#getType}
```
public int getType()
```


Microsoft Word alan türünü alır.

 **Examples:** 

Alan kodu kullanarak bir alanı belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
int - Microsoft Word alan türü. Döndürülen değer, [FieldType](../../com.aspose.words/fieldtype/) sabitlerinden biridir.
### isDirty() {#isDirty}
```
public boolean isDirty()
```


Belgenin diğer değişiklikleri nedeniyle alanın mevcut sonucunun artık doğru (eski) olup olmadığını alır.

 **Examples:** 

Alan sonucunu güncellemek için özel özelliğin nasıl kullanılacağını gösterir.

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
boolean - Alanın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru olmaması (eski) olup olmadığı.
### isDirty(boolean value) {#isDirty-boolean}
```
public void isDirty(boolean value)
```


Belgenin diğer değişiklikleri nedeniyle alanın mevcut sonucunun artık doğru (eski) olup olmadığını ayarlar.

 **Examples:** 

Alan sonucunu güncellemek için özel özelliğin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Alanın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru olmaması (eski) olup olmadığı. |

### isLocked() {#isLocked}
```
public boolean isLocked()
```


Alan kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır.

 **Examples:** 

Bir FieldStart düğümüyle nasıl çalışılacağını gösterir.

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
boolean - Alanın kilitli olup olmadığı (sonucunu yeniden hesaplamamalı).
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


Alan kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) ayarlar.

 **Examples:** 

Bir FieldStart düğümüyle nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Alanın kilitli olup olmadığı (sonucunu yeniden hesaplamamalı). |

### remove() {#remove}
```
public Node remove()
```


Alanı belgeden kaldırır. Alanın hemen sonrasında bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafı döndürür. Alan zaten kaldırılmışsa, null döndürür.

 **Examples:** 

Bir alan koleksiyonundan alanların nasıl kaldırılacağını gösterir.

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

PRIVATE alanların nasıl işleneceğini gösterir.

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


NW7 ve CODE39 barkod tipleri için Başlangıç/Bitiş karakterlerinin eklenip eklenmeyeceğini ayarlar.

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | NW7 ve CODE39 barkod tipleri için Başlat/Durdur karakterlerinin eklenip eklenmeyeceği. |

### setBackgroundColor(String value) {#setBackgroundColor-java.lang.String}
```
public void setBackgroundColor(String value)
```


Barkod sembolünün arka plan rengini ayarlar. Geçerli değerler [0, 0xFFFFFF] aralığındadır.

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Barkod sembolünün arka plan rengi. |

### setBarcodeType(String value) {#setBarcodeType-java.lang.String}
```
public void setBarcodeType(String value)
```


Barkod tipini (QR vb.) ayarlar

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Barkod tipi (QR vb.) |

### setBarcodeValue(String value) {#setBarcodeValue-java.lang.String}
```
public void setBarcodeValue(String value)
```


Barkod değerini ayarlar.

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Barkod değeri. |

### setCaseCodeStyle(String value) {#setCaseCodeStyle-java.lang.String}
```
public void setCaseCodeStyle(String value)
```


ITF14 barkod tipi için bir Kasa Kodu stilini ayarlar. Geçerli değerler [STD|EXT|ADD]

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | ITF14 barkod tipi için bir Kasa Kodu stili. |

### setDisplayText(boolean value) {#setDisplayText-boolean}
```
public void setDisplayText(boolean value)
```


Barkod verisinin (metin) görüntüyle birlikte gösterilip gösterilmeyeceğini ayarlar.

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Barkod verisinin (metin) görüntüyle birlikte gösterilip gösterilmeyeceği. |

### setErrorCorrectionLevel(String value) {#setErrorCorrectionLevel-java.lang.String}
```
public void setErrorCorrectionLevel(String value)
```


QR Kod için hata düzeltme seviyesini ayarlar. Geçerli değerler [0, 3].

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | QR Kod için bir hata düzeltme seviyesi. |

### setFixCheckDigit(boolean value) {#setFixCheckDigit-boolean}
```
public void setFixCheckDigit(boolean value)
```


Geçersiz olduğunda kontrol basamağının düzeltilip düzeltilmeyeceğini ayarlar.

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Kontrol rakamı geçersizse düzeltip düzeltmeyeceği. |

### setForegroundColor(String value) {#setForegroundColor-java.lang.String}
```
public void setForegroundColor(String value)
```


Barkod sembolünün ön plan rengini ayarlar. Geçerli değerler [0, 0xFFFFFF] aralığındadır.

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Barkod sembolünün ön plan rengi. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Alanının LCID'sini ayarlar.

 **Examples:** 

Bir alanı nasıl ekleyeceğinizi ve yerel ayarıyla nasıl çalışacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Alanın LCID'si. |

### setPosCodeStyle(String value) {#setPosCodeStyle-java.lang.String}
```
public void setPosCodeStyle(String value)
```


Satış Noktası barkodu stilini ayarlar (barkod tipleri UPCA|UPCE|EAN13|EAN8). Geçerli değerler (büyük/küçük harf duyarsız) [STD|SUP2|SUP5|CASE]

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Satış Noktası barkodu stili (barkod tipleri UPCA | UPCE | EAN13 | EAN8). |

### setResult(String value) {#setResult-java.lang.String}
```
public void setResult(String value)
```


Alan ayırıcı ile alan sonu arasındaki metni ayarlar.

 **Examples:** 

Alan kodu kullanarak bir alanı belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Alan ayırıcı ile alan sonu arasındaki metin. |

### setScalingFactor(String value) {#setScalingFactor-java.lang.String}
```
public void setScalingFactor(String value)
```


Sembol için bir ölçekleme faktörü ayarlar. Değer tam yüzde puanları cinsindendir ve geçerli değerler [10, 1000]

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Sembol için bir ölçekleme faktörü. |

### setSymbolHeight(String value) {#setSymbolHeight-java.lang.String}
```
public void setSymbolHeight(String value)
```


Sembolün yüksekliğini ayarlar. Birimler TWIPS'tir (1/1440 inç).

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Sembolün yüksekliği. |

### setSymbolRotation(String value) {#setSymbolRotation-java.lang.String}
```
public void setSymbolRotation(String value)
```


Barkod sembolünün dönüşünü ayarlar. Geçerli değerler [0, 3]'tür.

 **Examples:** 

DISPLAYBARCODE alanını nasıl ekleyeceğinizi ve özelliklerini nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Barkod sembolünün dönüşü. |

### unlink() {#unlink}
```
public boolean unlink()
```


Alan bağlantısını kaldırır.

 **Remarks:** 

Alanı en son sonucu ile değiştirir.

XE (Dizin Girişi) alanları ve SEQ (Sıra) alanları gibi bazı alanlar bağlantısı kesilemez.

 **Examples:** 

Bir alanın bağlantısını nasıl keseceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Linked fields.docx");
 doc.getRange().getFields().get(1).unlink();
 
```

**Returns:**
boolean -  true  ise alanın bağlantısı kesilmiş demektir, aksi takdirde  false .
### update() {#update}
```
public void update()
```


Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır.

 **Examples:** 

FieldType kullanarak bir alanı belgeye nasıl ekleyeceğinizi gösterir.

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

Alan sonuçlarını nasıl biçimlendireceğinizi gösterir.

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


Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır.

 **Examples:** 

Bir belge yüklenirken INCLUDEPICTURE alanlarını korumanın veya atmanın nasıl yapılacağını gösterir.

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
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ignoreMergeFormat | boolean | true ise, MERGEFORMAT anahtarına bakılmaksızın doğrudan alan sonucu biçimlendirmesi bırakılır, aksi takdirde normal güncelleme yapılır. |

