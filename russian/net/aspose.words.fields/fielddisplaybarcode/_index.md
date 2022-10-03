---
title: FieldDisplayBarcode
second_title: Справочник по API Aspose.Words для .NET
description: Реализует поле DISPLAYBARCODE.
type: docs
weight: 1650
url: /ru/net/aspose.words.fields/fielddisplaybarcode/
---
## FieldDisplayBarcode class

Реализует поле DISPLAYBARCODE.

```csharp
public class FieldDisplayBarcode : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldDisplayBarcode](fielddisplaybarcode/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AddStartStopChar](../../aspose.words.fields/fielddisplaybarcode/addstartstopchar/) { get; set; } | Получает или задает, следует ли добавлять символы Start/Stop для типов штрих-кодов NW7 и CODE39. |
| [BackgroundColor](../../aspose.words.fields/fielddisplaybarcode/backgroundcolor/) { get; set; } | Получает или задает цвет фона символа штрих-кода. Допустимые значения находятся в диапазоне [0, 0xFFFFFF] |
| [BarcodeType](../../aspose.words.fields/fielddisplaybarcode/barcodetype/) { get; set; } | Получает или задает тип штрих-кода (QR и т. д.) |
| [BarcodeValue](../../aspose.words.fields/fielddisplaybarcode/barcodevalue/) { get; set; } | Получает или задает значение штрих-кода. |
| [CaseCodeStyle](../../aspose.words.fields/fielddisplaybarcode/casecodestyle/) { get; set; } | Получает или задает стиль Case Code для штрих-кода типа ITF14. Допустимые значения: [STD&#x7C;EXT&#x7C;ADD] |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [DisplayText](../../aspose.words.fields/fielddisplaybarcode/displaytext/) { get; set; } | Получает или задает, отображать ли данные штрих-кода (текст) вместе с изображением. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [ErrorCorrectionLevel](../../aspose.words.fields/fielddisplaybarcode/errorcorrectionlevel/) { get; set; } | Получает или задает уровень исправления ошибок QR-кода. Допустимые значения: [0, 3]. |
| [FixCheckDigit](../../aspose.words.fields/fielddisplaybarcode/fixcheckdigit/) { get; set; } | Получает или задает, следует ли исправить контрольную цифру, если она недействительна. |
| [ForegroundColor](../../aspose.words.fields/fielddisplaybarcode/foregroundcolor/) { get; set; } | Получает или задает основной цвет символа штрих-кода. Допустимые значения находятся в диапазоне [0, 0xFFFFFF] |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/) объект, предоставляющий типизированный доступ к форматированию поля. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Получает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [PosCodeStyle](../../aspose.words.fields/fielddisplaybarcode/poscodestyle/) { get; set; } | Получает или задает стиль штрих-кода торговой точки (типы штрих-кода UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). Допустимые значения (без учета регистра): [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE]. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Получает или задает текст, который находится между разделителем поля и концом поля. |
| [ScalingFactor](../../aspose.words.fields/fielddisplaybarcode/scalingfactor/) { get; set; } | Получает или задает масштабный коэффициент для символа. Значение указано в целых процентах, допустимые значения: [10, 1000] . |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Может быть нулевым. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| [SymbolHeight](../../aspose.words.fields/fielddisplaybarcode/symbolheight/) { get; set; } | Получает или задает высоту символа. Единицы указаны в TWIPS (1/1440 дюйма). |
| [SymbolRotation](../../aspose.words.fields/fielddisplaybarcode/symbolrotation/) { get; set; } | Получает или задает поворот символа штрих-кода. Допустимые значения: [0, 3] |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). Включены как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает **нулевой** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет развязку поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Выполняет обновление поля. Выдает, если поле уже обновляется. |

### Примечания

Вставляет штрих-код.

### Примеры

Показывает, как выполнять слияние со штрих-кодами QR.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте поле MERGEBARCODE, которое будет принимать значения из источника данных во время слияния.
// Это поле преобразует все значения в столбце «MyQRCode» источника данных слияния в QR-коды.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "QR";
field.BarcodeValue = "MyQRCode";

// Применение пользовательских цветов и масштабирования.
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

// Создайте DataTable со столбцом с тем же именем, что и BarcodeValue нашего поля MERGEBARCODE.
// Слияние почты создаст новую страницу для каждой строки. Каждая страница будет содержать поле DISPLAYBARCODE,
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

Показывает, как вставить поле DISPLAYBARCODE и задать его свойства.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDisplayBarcode field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);

// Ниже приведены четыре типа штрих-кодов, оформленных по-разному, которые может отображать поле DISPLAYBARCODE.
// 1 - QR-код с пользовательскими цветами:
field.BarcodeType = "QR";
field.BarcodeValue = "ABC123";
field.BackgroundColor = "0xF8BD69";
field.ForegroundColor = "0xB5413B";
field.ErrorCorrectionLevel = "3";
field.ScalingFactor = "250";
field.SymbolHeight = "1000";
field.SymbolRotation = "0";

Assert.AreEqual(" DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0", field.GetFieldCode());
builder.Writeln();

// 2 - штрих-код EAN13 с цифрами, отображаемыми под штрихами:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "501234567890";
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// 3 - штрих-код CODE39:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "12345ABCDE";
field.AddStartStopChar = true;

Assert.AreEqual(" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// 4 - штрих-код ITF4, с указанным кодом случая:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "09312345678907";
field.CaseCodeStyle = "STD";

Assert.AreEqual(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.DISPLAYBARCODE.docx");
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
