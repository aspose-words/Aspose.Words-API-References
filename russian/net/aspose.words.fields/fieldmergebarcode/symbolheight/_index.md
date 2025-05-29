---
title: FieldMergeBarcode.SymbolHeight
linktitle: SymbolHeight
articleTitle: SymbolHeight
second_title: Aspose.Words для .NET
description: Отрегулируйте свойство FieldMergeBarcode SymbolHeight, чтобы настроить высоту штрихкода в TWIPS. Улучшите представление данных с точностью!
type: docs
weight: 130
url: /ru/net/aspose.words.fields/fieldmergebarcode/symbolheight/
---
## FieldMergeBarcode.SymbolHeight property

Возвращает или задает высоту символа. Единицы измерения — ТВИПС (1/1440 дюйма).

```csharp
public string SymbolHeight { get; set; }
```

## Примеры

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
