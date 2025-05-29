---
title: FieldMergeBarcode Class
linktitle: FieldMergeBarcode
articleTitle: FieldMergeBarcode
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldMergeBarcode, который позволяет легко реализовать поля MERGEBARCODE для повышения автоматизации и эффективности работы с документами.
type: docs
weight: 2550
url: /ru/net/aspose.words.fields/fieldmergebarcode/
---
## FieldMergeBarcode class

Реализует поле MERGEBARCODE.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class FieldMergeBarcode : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldMergeBarcode](fieldmergebarcode/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AddStartStopChar](../../aspose.words.fields/fieldmergebarcode/addstartstopchar/) { get; set; } | Возвращает или задает, следует ли добавлять символы Start/Stop для типов штрих-кодов NW7 и CODE39. |
| [BackgroundColor](../../aspose.words.fields/fieldmergebarcode/backgroundcolor/) { get; set; } | Получает или задает цвет фона символа штрих-кода. Допустимые значения находятся в диапазоне [0, 0xFFFFFF] |
| [BarcodeType](../../aspose.words.fields/fieldmergebarcode/barcodetype/) { get; set; } | Получает или задает тип штрихкода (QR и т. д.) |
| [BarcodeValue](../../aspose.words.fields/fieldmergebarcode/barcodevalue/) { get; set; } | Получает или задает значение штрих-кода. |
| [CaseCodeStyle](../../aspose.words.fields/fieldmergebarcode/casecodestyle/) { get; set; } | Получает или задает стиль Case Code для типа штрихкода ITF14. Допустимые значения: [STD&#x7C;EXT&#x7C;ADD] |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий отображаемый результат поля. |
| [DisplayText](../../aspose.words.fields/fieldmergebarcode/displaytext/) { get; set; } | Возвращает или задает, следует ли отображать данные штрих-кода (текст) вместе с изображением. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [ErrorCorrectionLevel](../../aspose.words.fields/fieldmergebarcode/errorcorrectionlevel/) { get; set; } | Получает или задает уровень исправления ошибок QR-кода. Допустимые значения: [0, 3]. |
| [FixCheckDigit](../../aspose.words.fields/fieldmergebarcode/fixcheckdigit/) { get; set; } | Возвращает или задает, следует ли исправлять контрольную цифру, если она недействительна. |
| [ForegroundColor](../../aspose.words.fields/fieldmergebarcode/foregroundcolor/) { get; set; } | Возвращает или задает цвет переднего плана символа штрихкода. Допустимые значения находятся в диапазоне [0, 0xFFFFFF] |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/)объект, который обеспечивает типизированный доступ к форматированию поля. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Возвращает или задает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Возвращает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [PosCodeStyle](../../aspose.words.fields/fieldmergebarcode/poscodestyle/) { get; set; } | Получает или задает стиль штрихкода точки продажи (типы штрихкодов UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). Допустимые значения (без учета регистра): [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE]. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Возвращает или задает текст, который находится между разделителем полей и концом поля. |
| [ScalingFactor](../../aspose.words.fields/fieldmergebarcode/scalingfactor/) { get; set; } | Возвращает или задает коэффициент масштабирования для символа. Значение указывается в целых процентных пунктах, допустимые значения: [10, 1000] |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Может быть`нулевой` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| [SymbolHeight](../../aspose.words.fields/fieldmergebarcode/symbolheight/) { get; set; } | Возвращает или задает высоту символа. Единицы измерения — ТВИПС (1/1440 дюйма). |
| [SymbolRotation](../../aspose.words.fields/fieldmergebarcode/symbolrotation/) { get; set; } | Получает или задает поворот символа штрих-кода. Допустимые значения: [0, 3] |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). Включаются как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля — последний child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает`нулевой` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет отмену связи поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |

## Примечания

Слияние штрих-кода.

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

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
