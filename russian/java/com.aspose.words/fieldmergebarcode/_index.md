---
title: "FieldMergeBarcode"
linktitle: "FieldMergeBarcode"
second_title: "Aspose.Words для Java"
description: "Реализует поле MERGEBARCODE в Java."
type: docs
weight: 257
url: /ru/java/com.aspose.words/fieldmergebarcode/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field/)
```
public class FieldMergeBarcode extends Field
```

Реализует поле MERGEBARCODE.

Чтобы узнать больше, посетите статью документации [ Working with Fields ][Working with Fields].

 **Remarks:** 

Слияние почты со штрих‑кодом.

 **Examples:** 

Показывает, как выполнить слияние почты для QR‑штрих‑кодов.

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

Показывает, как выполнить слияние почты для штрих‑кодов EAN13.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyEAN13Barcode" column into EAN13 barcodes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("MyEAN13Barcode");

 // Display the numeric value of the barcode underneath the bars.
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.getFieldCode());
 builder.writeln();

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display an EAN13 barcode with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyEAN13Barcode");
 table.getRows().add("501234567890");
 table.getRows().add("123456789012");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  123456789012 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.EAN13.docx");
 
```

Показывает, как выполнить слияние почты для штрих‑кодов CODE39.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyCODE39Barcode" column into CODE39 barcodes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("MyCODE39Barcode");

 // Edit its appearance to display start/stop characters.
 field.setAddStartStopChar(true);

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyCODE39Barcode CODE39 \\d", field.getFieldCode());
 builder.writeln();

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display a CODE39 barcode with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyCODE39Barcode");
 table.getRows().add("12345ABCDE");
 table.getRows().add("67890FGHIJ");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  12345ABCDE CODE39 \\d",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  67890FGHIJ CODE39 \\d",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.CODE39.docx");
 
```

Показывает, как выполнить слияние почты для штрих‑кодов ITF14.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyITF14Barcode" column into ITF14 barcodes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("MyITF14Barcode");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyITF14Barcode ITF14 \\c STD", field.getFieldCode());

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display an ITF14 barcode with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyITF14Barcode");
 table.getRows().add("09312345678907");
 table.getRows().add("1234567891234");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  1234567891234 ITF14 \\c STD",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.ITF14.docx");
 
```


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Методы

| Метод | Описание |
| --- | --- |
| [canWorkAsMergeField()](#canWorkAsMergeField) |  |
| [getAddStartStopChar()](#getAddStartStopChar) | Получает, следует ли добавлять символы начала/конца для типов штрих‑кодов NW7 и CODE39. |
| [getBackgroundColor()](#getBackgroundColor) | Получает цвет фона символа штрих‑кода. |
| [getBarcodeType()](#getBarcodeType) | Получает тип штрих‑кода (QR и др.) |
| [getBarcodeValue()](#getBarcodeValue) | Получает значение штрих‑кода. |
| [getCaseCodeStyle()](#getCaseCodeStyle) | Получает стиль кода Case для типа штрих‑кода ITF14. |
| [getDisplayResult()](#getDisplayResult) | Получает текст, представляющий отображаемый результат поля. |
| [getDisplayText()](#getDisplayText) | Получает, следует ли отображать данные штрих‑кода (текст) вместе с изображением. |
| [getEnd()](#getEnd) | Получает узел, представляющий конец поля. |
| [getErrorCorrectionLevel()](#getErrorCorrectionLevel) | Получает уровень коррекции ошибок QR‑кода. |
| [getFieldCode()](#getFieldCode) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [getFixCheckDigit()](#getFixCheckDigit) | Получает, следует ли исправлять контрольную цифру, если она недействительна. |
| [getForegroundColor()](#getForegroundColor) | Получает цвет переднего плана символа штрих‑кода. |
| [getFormat()](#getFormat) | Получает объект [FieldFormat](../../com.aspose.words/fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [getLocaleId()](#getLocaleId) | Получает LCID поля. |
| [getMergeFieldName()](#getMergeFieldName) |  |
| [getPosCodeStyle()](#getPosCodeStyle) | Gets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). |
| [getResult()](#getResult) | Получает текст, находящийся между разделителем поля и концом поля. |
| [getScalingFactor()](#getScalingFactor) | Получает коэффициент масштабирования символа. |
| [getSeparator()](#getSeparator) | Получает узел, представляющий разделитель поля. |
| [getStart()](#getStart) | Получает узел, представляющий начало поля. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getSymbolHeight()](#getSymbolHeight) | Получает высоту символа. |
| [getSymbolRotation()](#getSymbolRotation) | Получает вращение символа штрих‑кода. |
| [getType()](#getType) | Получает тип поля Microsoft Word. |
| [isDirty()](#isDirty) | Определяет, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [isDirty(boolean value)](#isDirty-boolean) | Устанавливает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [isLocked()](#isLocked) | Определяет, заблокировано ли поле (не должно пересчитывать свой результат). |
| [isLocked(boolean value)](#isLocked-boolean) | Устанавливает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [isMergeValueRequired()](#isMergeValueRequired) |  |
| [remove()](#remove) | Удаляет поле из документа. |
| [setAddStartStopChar(boolean value)](#setAddStartStopChar-boolean) | Устанавливает, следует ли добавлять символы начала/конца для типов штрих‑кодов NW7 и CODE39. |
| [setBackgroundColor(String value)](#setBackgroundColor-java.lang.String) | Устанавливает цвет фона символа штрих‑кода. |
| [setBarcodeType(String value)](#setBarcodeType-java.lang.String) | Устанавливает тип штрихкода (QR и др.) |
| [setBarcodeValue(String value)](#setBarcodeValue-java.lang.String) | Устанавливает значение штрихкода. |
| [setCaseCodeStyle(String value)](#setCaseCodeStyle-java.lang.String) | Устанавливает стиль кода упаковки для типа штрихкода ITF14. |
| [setDisplayText(boolean value)](#setDisplayText-boolean) | Устанавливает, отображать ли данные штрихкода (текст) вместе с изображением. |
| [setErrorCorrectionLevel(String value)](#setErrorCorrectionLevel-java.lang.String) | Устанавливает уровень коррекции ошибок QR‑кода. |
| [setFixCheckDigit(boolean value)](#setFixCheckDigit-boolean) | Устанавливает, исправлять ли контрольную цифру, если она недействительна. |
| [setForegroundColor(String value)](#setForegroundColor-java.lang.String) | Устанавливает цвет переднего плана символа штрихкода. |
| [setLocaleId(int value)](#setLocaleId-int) | Устанавливает LCID поля. |
| [setPosCodeStyle(String value)](#setPosCodeStyle-java.lang.String) | Sets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). |
| [setResult(String value)](#setResult-java.lang.String) | Устанавливает текст, находящийся между разделителем поля и его концом. |
| [setScalingFactor(String value)](#setScalingFactor-java.lang.String) | Устанавливает коэффициент масштабирования символа. |
| [setSymbolHeight(String value)](#setSymbolHeight-java.lang.String) | Устанавливает высоту символа. |
| [setSymbolRotation(String value)](#setSymbolRotation-java.lang.String) | Устанавливает вращение символа штрихкода. |
| [unlink()](#unlink) | Выполняет разъединение поля. |
| [update()](#update) | Выполняет обновление поля. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | Выполняет обновление поля. |
### canWorkAsMergeField() {#canWorkAsMergeField}
```
public boolean canWorkAsMergeField()
```




**Returns:**
boolean
### getAddStartStopChar() {#getAddStartStopChar}
```
public boolean getAddStartStopChar()
```


Получает, следует ли добавлять символы начала/конца для типов штрих‑кодов NW7 и CODE39.

 **Examples:** 

Показывает, как выполнить слияние почты для штрих‑кодов CODE39.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyCODE39Barcode" column into CODE39 barcodes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("MyCODE39Barcode");

 // Edit its appearance to display start/stop characters.
 field.setAddStartStopChar(true);

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyCODE39Barcode CODE39 \\d", field.getFieldCode());
 builder.writeln();

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display a CODE39 barcode with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyCODE39Barcode");
 table.getRows().add("12345ABCDE");
 table.getRows().add("67890FGHIJ");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  12345ABCDE CODE39 \\d",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  67890FGHIJ CODE39 \\d",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.CODE39.docx");
 
```

**Returns:**
boolean — Добавлять ли символы начала/конца для типов штрихкода NW7 и CODE39.
### getBackgroundColor() {#getBackgroundColor}
```
public String getBackgroundColor()
```


Получает цвет фона символа штрихкода. Допустимые значения находятся в диапазоне [0, 0xFFFFFF]

 **Examples:** 

Показывает, как выполнить слияние почты для QR‑штрих‑кодов.

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

**Returns:**
java.lang.String — Цвет фона символа штрихкода.
### getBarcodeType() {#getBarcodeType}
```
public String getBarcodeType()
```


Получает тип штрих‑кода (QR и др.)

 **Examples:** 

Показывает, как выполнить слияние почты для QR‑штрих‑кодов.

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

Показывает, как выполнить слияние почты для штрих‑кодов EAN13.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyEAN13Barcode" column into EAN13 barcodes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("MyEAN13Barcode");

 // Display the numeric value of the barcode underneath the bars.
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.getFieldCode());
 builder.writeln();

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display an EAN13 barcode with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyEAN13Barcode");
 table.getRows().add("501234567890");
 table.getRows().add("123456789012");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  123456789012 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.EAN13.docx");
 
```

Показывает, как выполнить слияние почты для штрих‑кодов CODE39.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyCODE39Barcode" column into CODE39 barcodes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("MyCODE39Barcode");

 // Edit its appearance to display start/stop characters.
 field.setAddStartStopChar(true);

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyCODE39Barcode CODE39 \\d", field.getFieldCode());
 builder.writeln();

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display a CODE39 barcode with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyCODE39Barcode");
 table.getRows().add("12345ABCDE");
 table.getRows().add("67890FGHIJ");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  12345ABCDE CODE39 \\d",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  67890FGHIJ CODE39 \\d",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.CODE39.docx");
 
```

Показывает, как выполнить слияние почты для штрих‑кодов ITF14.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyITF14Barcode" column into ITF14 barcodes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("MyITF14Barcode");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyITF14Barcode ITF14 \\c STD", field.getFieldCode());

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display an ITF14 barcode with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyITF14Barcode");
 table.getRows().add("09312345678907");
 table.getRows().add("1234567891234");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  1234567891234 ITF14 \\c STD",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.ITF14.docx");
 
```

**Returns:**
java.lang.String — Тип штрихкода (QR и др.)
### getBarcodeValue() {#getBarcodeValue}
```
public String getBarcodeValue()
```


Получает значение штрих‑кода.

 **Examples:** 

Показывает, как выполнить слияние почты для QR‑штрих‑кодов.

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

Показывает, как выполнить слияние почты для штрих‑кодов EAN13.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyEAN13Barcode" column into EAN13 barcodes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("MyEAN13Barcode");

 // Display the numeric value of the barcode underneath the bars.
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.getFieldCode());
 builder.writeln();

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display an EAN13 barcode with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyEAN13Barcode");
 table.getRows().add("501234567890");
 table.getRows().add("123456789012");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  123456789012 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.EAN13.docx");
 
```

**Returns:**
java.lang.String — Значение штрихкода.
### getCaseCodeStyle() {#getCaseCodeStyle}
```
public String getCaseCodeStyle()
```


Получает стиль кода упаковки для типа штрихкода ITF14. Допустимые значения: [STD|EXT|ADD]

 **Examples:** 

Показывает, как выполнить слияние почты для штрих‑кодов ITF14.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyITF14Barcode" column into ITF14 barcodes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("MyITF14Barcode");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyITF14Barcode ITF14 \\c STD", field.getFieldCode());

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display an ITF14 barcode with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyITF14Barcode");
 table.getRows().add("09312345678907");
 table.getRows().add("1234567891234");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  1234567891234 ITF14 \\c STD",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.ITF14.docx");
 
```

**Returns:**
java.lang.String — Стиль кода упаковки для типа штрихкода ITF14.
### getDisplayResult() {#getDisplayResult}
```
public String getDisplayResult()
```


Получает текст, представляющий отображаемый результат поля.

 **Remarks:** 

Метод [Document.updateListLabels()](../../com.aspose.words/document/\#updateListLabels) должен быть вызван для получения корректного значения полей [FieldListNum](../../com.aspose.words/fieldlistnum/), [FieldAutoNum](../../com.aspose.words/fieldautonum/), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout/) и [FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl/).

 **Examples:** 

Показывает, как получить реальный текст, который поле отображает в документе.

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
java.lang.String — Текст, представляющий отображаемый результат поля.
### getDisplayText() {#getDisplayText}
```
public boolean getDisplayText()
```


Получает, следует ли отображать данные штрих‑кода (текст) вместе с изображением.

 **Examples:** 

Показывает, как выполнить слияние почты для штрих‑кодов EAN13.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyEAN13Barcode" column into EAN13 barcodes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("MyEAN13Barcode");

 // Display the numeric value of the barcode underneath the bars.
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.getFieldCode());
 builder.writeln();

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display an EAN13 barcode with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyEAN13Barcode");
 table.getRows().add("501234567890");
 table.getRows().add("123456789012");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  123456789012 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.EAN13.docx");
 
```

**Returns:**
boolean — Отображать ли данные штрихкода (текст) вместе с изображением.
### getEnd() {#getEnd}
```
public FieldEnd getEnd()
```


Получает узел, представляющий конец поля.

 **Examples:** 

Показывает, как работать с коллекцией полей.

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


Получает уровень коррекции ошибок QR‑кода. Допустимые значения: [0, 3].

 **Examples:** 

Показывает, как выполнить слияние почты для QR‑штрих‑кодов.

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

**Returns:**
java.lang.String — Уровень коррекции ошибок QR‑кода.
### getFieldCode() {#getFieldCode}
```
public String getFieldCode()
```


Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включаются как код поля, так и результат дочерних полей.

 **Examples:** 

Показывает, как вставить поле в документ, используя код поля.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

Показывает, как получить код поля.

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


Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует).

 **Examples:** 

Показывает, как получить код поля.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| includeChildFieldCodes | boolean | true, если коды дочерних полей должны быть включены. |

**Returns:**
java.lang.String
### getFixCheckDigit() {#getFixCheckDigit}
```
public boolean getFixCheckDigit()
```


Получает, следует ли исправлять контрольную цифру, если она недействительна.

 **Examples:** 

Показывает, как выполнить слияние почты для штрих‑кодов EAN13.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyEAN13Barcode" column into EAN13 barcodes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("MyEAN13Barcode");

 // Display the numeric value of the barcode underneath the bars.
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.getFieldCode());
 builder.writeln();

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display an EAN13 barcode with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyEAN13Barcode");
 table.getRows().add("501234567890");
 table.getRows().add("123456789012");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  123456789012 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.EAN13.docx");
 
```

**Returns:**
boolean — Исправлять ли контрольную цифру, если она недействительна.
### getForegroundColor() {#getForegroundColor}
```
public String getForegroundColor()
```


Получает цвет переднего плана символа штрихкода. Допустимые значения находятся в диапазоне [0, 0xFFFFFF]

 **Examples:** 

Показывает, как выполнить слияние почты для QR‑штрих‑кодов.

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

**Returns:**
java.lang.String — Цвет переднего плана символа штрихкода.
### getFormat() {#getFormat}
```
public FieldFormat getFormat()
```


Получает объект [FieldFormat](../../com.aspose.words/fieldformat/), который предоставляет типизированный доступ к форматированию поля.

 **Examples:** 

Показывает, как форматировать результаты полей.

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


Получает LCID поля.

 **Examples:** 

Показывает, как вставить поле и работать с его локалью.

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
int - LCID поля.
### getMergeFieldName() {#getMergeFieldName}
```
public String getMergeFieldName()
```




**Returns:**
java.lang.String
### getPosCodeStyle() {#getPosCodeStyle}
```
public String getPosCodeStyle()
```


Получает стиль штрихкода точки продаж (типы штрихкода UPCA|UPCE|EAN13|EAN8). Допустимые значения (без учёта регистра): [STD|SUP2|SUP5|CASE].

 **Examples:** 

Показывает, как выполнить слияние почты для штрих‑кодов EAN13.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyEAN13Barcode" column into EAN13 barcodes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("MyEAN13Barcode");

 // Display the numeric value of the barcode underneath the bars.
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.getFieldCode());
 builder.writeln();

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display an EAN13 barcode with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyEAN13Barcode");
 table.getRows().add("501234567890");
 table.getRows().add("123456789012");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  123456789012 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.EAN13.docx");
 
```

**Returns:**
java.lang.String — Стиль штрихкода точки продаж (типы штрихкода UPCA|UPCE|EAN13|EAN8).
### getResult() {#getResult}
```
public String getResult()
```


Получает текст, находящийся между разделителем поля и концом поля.

 **Examples:** 

Показывает, как вставить поле в документ, используя код поля.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
java.lang.String - Текст, который находится между разделителем поля и его концом.
### getScalingFactor() {#getScalingFactor}
```
public String getScalingFactor()
```


Получает коэффициент масштабирования для символа. Значение задаётся в целых процентных пунктах, допустимые значения: [10, 1000]

 **Examples:** 

Показывает, как выполнить слияние почты для QR‑штрих‑кодов.

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

**Returns:**
java.lang.String - Коэффициент масштабирования для символа.
### getSeparator() {#getSeparator}
```
public FieldSeparator getSeparator()
```


Получает узел, представляющий разделитель поля. Может быть  null .

 **Examples:** 

Показывает, как работать с коллекцией полей.

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


Получает узел, представляющий начало поля.

 **Examples:** 

Показывает, как работать с коллекцией полей.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Returns:**
int
### getSymbolHeight() {#getSymbolHeight}
```
public String getSymbolHeight()
```


Получает высоту символа. Единицы измерения — TWIPS (1/1440 дюйма).

 **Examples:** 

Показывает, как выполнить слияние почты для QR‑штрих‑кодов.

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

**Returns:**
java.lang.String - Высота символа.
### getSymbolRotation() {#getSymbolRotation}
```
public String getSymbolRotation()
```


Получает вращение символа штрихкода. Допустимые значения: [0, 3]

 **Examples:** 

Показывает, как выполнить слияние почты для QR‑штрих‑кодов.

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

**Returns:**
java.lang.String - Вращение символа штрихкода.
### getType() {#getType}
```
public int getType()
```


Получает тип поля Microsoft Word.

 **Examples:** 

Показывает, как вставить поле в документ, используя код поля.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
int - Тип поля Microsoft Word. Возвращаемое значение является одной из констант [FieldType](../../com.aspose.words/fieldtype/).
### isDirty() {#isDirty}
```
public boolean isDirty()
```


Определяет, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ.

 **Examples:** 

Показывает, как использовать специальное свойство для обновления результата поля.

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
boolean - Является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ.
### isDirty(boolean value) {#isDirty-boolean}
```
public void isDirty(boolean value)
```


Устанавливает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ.

 **Examples:** 

Показывает, как использовать специальное свойство для обновления результата поля.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |

### isLocked() {#isLocked}
```
public boolean isLocked()
```


Определяет, заблокировано ли поле (не должно пересчитывать свой результат).

 **Examples:** 

Показывает, как работать с узлом FieldStart.

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
boolean - Является ли поле заблокированным (не должно пересчитывать свой результат).
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


Устанавливает, заблокировано ли поле (не должно пересчитывать свой результат).

 **Examples:** 

Показывает, как работать с узлом FieldStart.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Является ли поле заблокированным (не должно пересчитывать свой результат). |

### isMergeValueRequired() {#isMergeValueRequired}
```
public boolean isMergeValueRequired()
```




**Returns:**
boolean
### remove() {#remove}
```
public Node remove()
```


Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает  null .

 **Examples:** 

Показывает, как удалять поля из коллекции полей.

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

Показывает, как обрабатывать поля PRIVATE.

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


Устанавливает, следует ли добавлять символы начала/конца для типов штрих‑кодов NW7 и CODE39.

 **Examples:** 

Показывает, как выполнить слияние почты для штрих‑кодов CODE39.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyCODE39Barcode" column into CODE39 barcodes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("MyCODE39Barcode");

 // Edit its appearance to display start/stop characters.
 field.setAddStartStopChar(true);

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyCODE39Barcode CODE39 \\d", field.getFieldCode());
 builder.writeln();

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display a CODE39 barcode with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyCODE39Barcode");
 table.getRows().add("12345ABCDE");
 table.getRows().add("67890FGHIJ");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  12345ABCDE CODE39 \\d",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  67890FGHIJ CODE39 \\d",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.CODE39.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Нужно ли добавлять символы Start/Stop для типов штрихкодов NW7 и CODE39. |

### setBackgroundColor(String value) {#setBackgroundColor-java.lang.String}
```
public void setBackgroundColor(String value)
```


Устанавливает фоновый цвет символа штрихкода. Допустимые значения в диапазоне [0, 0xFFFFFF]

 **Examples:** 

Показывает, как выполнить слияние почты для QR‑штрих‑кодов.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Фоновый цвет символа штрихкода. |

### setBarcodeType(String value) {#setBarcodeType-java.lang.String}
```
public void setBarcodeType(String value)
```


Устанавливает тип штрихкода (QR и др.)

 **Examples:** 

Показывает, как выполнить слияние почты для QR‑штрих‑кодов.

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

Показывает, как выполнить слияние почты для штрих‑кодов EAN13.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyEAN13Barcode" column into EAN13 barcodes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("MyEAN13Barcode");

 // Display the numeric value of the barcode underneath the bars.
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.getFieldCode());
 builder.writeln();

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display an EAN13 barcode with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyEAN13Barcode");
 table.getRows().add("501234567890");
 table.getRows().add("123456789012");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  123456789012 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.EAN13.docx");
 
```

Показывает, как выполнить слияние почты для штрих‑кодов CODE39.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyCODE39Barcode" column into CODE39 barcodes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("CODE39");
 field.setBarcodeValue("MyCODE39Barcode");

 // Edit its appearance to display start/stop characters.
 field.setAddStartStopChar(true);

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyCODE39Barcode CODE39 \\d", field.getFieldCode());
 builder.writeln();

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display a CODE39 barcode with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyCODE39Barcode");
 table.getRows().add("12345ABCDE");
 table.getRows().add("67890FGHIJ");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  12345ABCDE CODE39 \\d",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  67890FGHIJ CODE39 \\d",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.CODE39.docx");
 
```

Показывает, как выполнить слияние почты для штрих‑кодов ITF14.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyITF14Barcode" column into ITF14 barcodes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("MyITF14Barcode");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyITF14Barcode ITF14 \\c STD", field.getFieldCode());

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display an ITF14 barcode with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyITF14Barcode");
 table.getRows().add("09312345678907");
 table.getRows().add("1234567891234");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  1234567891234 ITF14 \\c STD",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.ITF14.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Тип штрихкода (QR и др.) |

### setBarcodeValue(String value) {#setBarcodeValue-java.lang.String}
```
public void setBarcodeValue(String value)
```


Устанавливает значение штрихкода.

 **Examples:** 

Показывает, как выполнить слияние почты для QR‑штрих‑кодов.

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

Показывает, как выполнить слияние почты для штрих‑кодов EAN13.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyEAN13Barcode" column into EAN13 barcodes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("MyEAN13Barcode");

 // Display the numeric value of the barcode underneath the bars.
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.getFieldCode());
 builder.writeln();

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display an EAN13 barcode with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyEAN13Barcode");
 table.getRows().add("501234567890");
 table.getRows().add("123456789012");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  123456789012 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.EAN13.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Значение штрихкода. |

### setCaseCodeStyle(String value) {#setCaseCodeStyle-java.lang.String}
```
public void setCaseCodeStyle(String value)
```


Устанавливает стиль Case Code для штрихкода типа ITF14. Допустимые значения: [STD|EXT|ADD]

 **Examples:** 

Показывает, как выполнить слияние почты для штрих‑кодов ITF14.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyITF14Barcode" column into ITF14 barcodes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("ITF14");
 field.setBarcodeValue("MyITF14Barcode");
 field.setCaseCodeStyle("STD");

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyITF14Barcode ITF14 \\c STD", field.getFieldCode());

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display an ITF14 barcode with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyITF14Barcode");
 table.getRows().add("09312345678907");
 table.getRows().add("1234567891234");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  1234567891234 ITF14 \\c STD",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.ITF14.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Стиль Case Code для штрихкода типа ITF14. |

### setDisplayText(boolean value) {#setDisplayText-boolean}
```
public void setDisplayText(boolean value)
```


Устанавливает, отображать ли данные штрихкода (текст) вместе с изображением.

 **Examples:** 

Показывает, как выполнить слияние почты для штрих‑кодов EAN13.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyEAN13Barcode" column into EAN13 barcodes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("MyEAN13Barcode");

 // Display the numeric value of the barcode underneath the bars.
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.getFieldCode());
 builder.writeln();

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display an EAN13 barcode with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyEAN13Barcode");
 table.getRows().add("501234567890");
 table.getRows().add("123456789012");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  123456789012 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.EAN13.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Отображать ли данные штрихкода (текст) вместе с изображением. |

### setErrorCorrectionLevel(String value) {#setErrorCorrectionLevel-java.lang.String}
```
public void setErrorCorrectionLevel(String value)
```


Устанавливает уровень коррекции ошибок QR‑кода. Допустимые значения: [0, 3].

 **Examples:** 

Показывает, как выполнить слияние почты для QR‑штрих‑кодов.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Уровень коррекции ошибок QR‑кода. |

### setFixCheckDigit(boolean value) {#setFixCheckDigit-boolean}
```
public void setFixCheckDigit(boolean value)
```


Устанавливает, исправлять ли контрольную цифру, если она недействительна.

 **Examples:** 

Показывает, как выполнить слияние почты для штрих‑кодов EAN13.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyEAN13Barcode" column into EAN13 barcodes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("MyEAN13Barcode");

 // Display the numeric value of the barcode underneath the bars.
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.getFieldCode());
 builder.writeln();

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display an EAN13 barcode with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyEAN13Barcode");
 table.getRows().add("501234567890");
 table.getRows().add("123456789012");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  123456789012 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.EAN13.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Нужно ли исправлять контрольную цифру, если она недействительна. |

### setForegroundColor(String value) {#setForegroundColor-java.lang.String}
```
public void setForegroundColor(String value)
```


Устанавливает передний (основной) цвет символа штрихкода. Допустимые значения в диапазоне [0, 0xFFFFFF]

 **Examples:** 

Показывает, как выполнить слияние почты для QR‑штрих‑кодов.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Основной цвет символа штрихкода. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Устанавливает LCID поля.

 **Examples:** 

Показывает, как вставить поле и работать с его локалью.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | LCID поля. |

### setPosCodeStyle(String value) {#setPosCodeStyle-java.lang.String}
```
public void setPosCodeStyle(String value)
```


Устанавливает стиль POS‑штрихкода (типы штрихкодов UPCA|UPCE|EAN13|EAN8). Допустимые значения (без учёта регистра): [STD|SUP2|SUP5|CASE].

 **Examples:** 

Показывает, как выполнить слияние почты для штрих‑кодов EAN13.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
 // This field will convert all values in a merge data source's "MyEAN13Barcode" column into EAN13 barcodes.
 FieldMergeBarcode field = (FieldMergeBarcode) builder.insertField(FieldType.FIELD_MERGE_BARCODE, true);
 field.setBarcodeType("EAN13");
 field.setBarcodeValue("MyEAN13Barcode");

 // Display the numeric value of the barcode underneath the bars.
 field.setDisplayText(true);
 field.setPosCodeStyle("CASE");
 field.setFixCheckDigit(true);

 Assert.assertEquals(FieldType.FIELD_MERGE_BARCODE, field.getType());
 Assert.assertEquals(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.getFieldCode());
 builder.writeln();

 // Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
 // The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
 // which will display an EAN13 barcode with the value from the merged row.
 DataTable table = new DataTable("Barcodes");
 table.getColumns().add("MyEAN13Barcode");
 table.getRows().add("501234567890");
 table.getRows().add("123456789012");

 doc.getMailMerge().execute(table);

 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(0).getType());
 Assert.assertEquals(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DISPLAY_BARCODE, doc.getRange().getFields().get(1).getType());
 Assert.assertEquals(" DISPLAYBARCODE  123456789012 EAN13 \\t \\p CASE \\x",
         doc.getRange().getFields().get(1).getFieldCode());

 doc.save(getArtifactsDir() + "Field.MERGEBARCODE.EAN13.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Стиль POS‑штрихкода (типы штрихкодов UPCA | UPCE | EAN13 | EAN8). |

### setResult(String value) {#setResult-java.lang.String}
```
public void setResult(String value)
```


Устанавливает текст, находящийся между разделителем поля и его концом.

 **Examples:** 

Показывает, как вставить поле в документ, используя код поля.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Текст, который находится между разделителем поля и его концом. |

### setScalingFactor(String value) {#setScalingFactor-java.lang.String}
```
public void setScalingFactor(String value)
```


Устанавливает коэффициент масштабирования для символа. Значение задаётся в целых процентных пунктах, допустимые значения: [10, 1000]

 **Examples:** 

Показывает, как выполнить слияние почты для QR‑штрих‑кодов.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Коэффициент масштабирования символа. |

### setSymbolHeight(String value) {#setSymbolHeight-java.lang.String}
```
public void setSymbolHeight(String value)
```


Устанавливает высоту символа. Единицы измерения — TWIPS (1/1440 дюйма).

 **Examples:** 

Показывает, как выполнить слияние почты для QR‑штрих‑кодов.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Высота символа. |

### setSymbolRotation(String value) {#setSymbolRotation-java.lang.String}
```
public void setSymbolRotation(String value)
```


Устанавливает вращение штрихкода. Допустимые значения — [0, 3]

 **Examples:** 

Показывает, как выполнить слияние почты для QR‑штрих‑кодов.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Вращение штрихкода. |

### unlink() {#unlink}
```
public boolean unlink()
```


Выполняет разъединение поля.

 **Remarks:** 

Заменяет поле его самым последним результатом.

Некоторые поля, такие как поля XE (Index Entry) и SEQ (Sequence), нельзя разъединять.

 **Examples:** 

Показывает, как разъединить поле.

```

 Document doc = new Document(getMyDir() + "Linked fields.docx");
 doc.getRange().getFields().get(1).unlink();
 
```

**Returns:**
boolean -  true  если поле было разъединено, иначе  false .
### update() {#update}
```
public void update()
```


Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется.

 **Examples:** 

Показывает, как вставить поле в документ, используя FieldType.

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

Показывает, как форматировать результаты полей.

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


Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется.

 **Examples:** 

Показывает, как сохранять или отбрасывать поля INCLUDEPICTURE при загрузке документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| ignoreMergeFormat | boolean | Если  true  то прямое форматирование результата поля отменяется, независимо от переключателя MERGEFORMAT, иначе выполняется обычное обновление. |

