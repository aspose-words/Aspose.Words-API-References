---
title: FieldMergeBarcode.BarcodeType
linktitle: BarcodeType
articleTitle: BarcodeType
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldMergeBarcode BarcodeType, позволяющее легко управлять и настраивать различные типы штрихкодов, такие как QR, для улучшенной интеграции данных.
type: docs
weight: 40
url: /ru/net/aspose.words.fields/fieldmergebarcode/barcodetype/
---
## FieldMergeBarcode.BarcodeType property

Получает или задает тип штрихкода (QR и т. д.)

```csharp
public string BarcodeType { get; set; }
```

## Примеры

Показывает, как выполнить слияние почты со штрихкодами ITF14.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте поле MERGEBARCODE, которое будет принимать значения из источника данных во время слияния почты.
// Это поле преобразует все значения в столбце «MyITF14Barcode» источника объединенных данных в штрихкоды ITF14.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "MyITF14Barcode";
field.CaseCodeStyle = "STD";

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyITF14Barcode ITF14 \\c STD", field.GetFieldCode());

// Создаем DataTable со столбцом с тем же именем, что и BarcodeValue нашего поля MERGEBARCODE.
// Слияние создаст новую страницу для каждой строки. Каждая страница будет содержать поле DISPLAYBARCODE,
// который отобразит штрих-код ITF14 со значением из объединенной строки.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyITF14Barcode");
table.Rows.Add(new[] { "09312345678907" });
table.Rows.Add(new[] { "1234567891234" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"09312345678907\" ITF14 \\c STD",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"1234567891234\" ITF14 \\c STD",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.ITF14.docx");
```

Показывает, как выполнить слияние писем по штрих-кодам CODE39.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте поле MERGEBARCODE, которое будет принимать значения из источника данных во время слияния почты.
// Это поле преобразует все значения в столбце «MyCODE39Barcode» источника объединенных данных в штрихкоды CODE39.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "MyCODE39Barcode";

// Отредактируйте его внешний вид для отображения начальных/конечных символов.
field.AddStartStopChar = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyCODE39Barcode CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// Создаем DataTable со столбцом с тем же именем, что и BarcodeValue нашего поля MERGEBARCODE.
// Слияние создаст новую страницу для каждой строки. Каждая страница будет содержать поле DISPLAYBARCODE,
// который отобразит штрих-код CODE39 со значением из объединенной строки.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyCODE39Barcode");
table.Rows.Add(new[] { "12345ABCDE" });
table.Rows.Add(new[] { "67890FGHIJ" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"12345ABCDE\" CODE39 \\d",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"67890FGHIJ\" CODE39 \\d",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.CODE39.docx");
```

Показывает, как выполнить слияние писем со штрихкодами EAN13.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте поле MERGEBARCODE, которое будет принимать значения из источника данных во время слияния почты.
// Это поле преобразует все значения в столбце «MyEAN13Barcode» источника объединенных данных в штрихкоды EAN13.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "MyEAN13Barcode";

// Отображаем числовое значение штрих-кода под полосами.
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// Создаем DataTable со столбцом с тем же именем, что и BarcodeValue нашего поля MERGEBARCODE.
// Слияние создаст новую страницу для каждой строки. Каждая страница будет содержать поле DISPLAYBARCODE,
// который отобразит штрих-код EAN13 со значением из объединенной строки.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyEAN13Barcode");
table.Rows.Add(new[] { "501234567890" });
table.Rows.Add(new[] { "123456789012" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"501234567890\" EAN13 \\t \\p CASE \\x",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"123456789012\" EAN13 \\t \\p CASE \\x",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.EAN13.docx");
```

Показывает, как выполнить слияние писем с QR-штрихкодами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте поле MERGEBARCODE, которое будет принимать значения из источника данных во время слияния почты.
// Это поле преобразует все значения в столбце «MyQRCode» источника объединенных данных в QR-коды.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "QR";
field.BarcodeValue = "MyQRCode";

// Применить пользовательские цвета и масштабирование.
field.BackgroundColor = "0xF8BD69";
field.ForegroundColor = "0xB5413B";
field.ErrorCorrectionLevel = "3";
field.ScalingFactor = "250";
field.SymbolHeight = "1000";
field.SymbolRotation = "0";

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyQRCode QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0",
    field.GetFieldCode());
builder.Writeln();

// Создаем DataTable со столбцом с тем же именем, что и BarcodeValue нашего поля MERGEBARCODE.
// Слияние создаст новую страницу для каждой строки. Каждая страница будет содержать поле DISPLAYBARCODE,
// который отобразит QR-код со значением из объединенной строки.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyQRCode");
table.Rows.Add(new[] { "ABC123" });
table.Rows.Add(new[] { "DEF456" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"ABC123\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B", 
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"DEF456\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.QR.docx");
```

### Смотрите также

* class [FieldMergeBarcode](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
