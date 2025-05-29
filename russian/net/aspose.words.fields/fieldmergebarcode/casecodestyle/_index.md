---
title: FieldMergeBarcode.CaseCodeStyle
linktitle: CaseCodeStyle
articleTitle: CaseCodeStyle
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldMergeBarcode CaseCodeStyle для штрихкодов ITF14. Легко настройте свой стиль Case Code с допустимыми параметрами, такими как STDEXTADD.
type: docs
weight: 60
url: /ru/net/aspose.words.fields/fieldmergebarcode/casecodestyle/
---
## FieldMergeBarcode.CaseCodeStyle property

Получает или задает стиль Case Code для типа штрихкода ITF14. Допустимые значения: [STD&#x7C;EXT&#x7C;ADD]

```csharp
public string CaseCodeStyle { get; set; }
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

### Смотрите также

* class [FieldMergeBarcode](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
