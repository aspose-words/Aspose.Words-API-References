---
title: FieldBarcode.IsBookmark
second_title: Справочник по API Aspose.Words для .NET
description: FieldBarcode свойство. Получает или устанавливаетPostalAddress имя закладки.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldbarcode/isbookmark/
---
## FieldBarcode.IsBookmark property

Получает или устанавливает,[`PostalAddress`](../postaladdress/) имя закладки.

```csharp
public bool IsBookmark { get; set; }
```

### Примеры

Показывает, как использовать поле ШТРИХ-КОД для отображения почтовых индексов США в виде штрих-кода.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Ниже приведены два способа использования полей ШТРИХ-КОДА для отображения пользовательских значений в виде штрих-кодов.
// 1 - Сохраняем значение, которое будет отображаться штрих-кодом в свойстве PostalAddress:
FieldBarcode field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);

// Это значение должно быть допустимым почтовым индексом.
field.PostalAddress = "96801";
field.IsUSPostalAddress = true;
field.FacingIdentificationMark = "C";

Assert.AreEqual(" BARCODE  96801 \\u \\f C", field.GetFieldCode());

builder.InsertBreak(BreakType.LineBreak);

// 2 - Ссылка на закладку, в которой хранится значение, которое будет отображать этот штрих-код:
field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);
field.PostalAddress = "BarcodeBookmark";
field.IsBookmark = true;

Assert.AreEqual(" BARCODE  BarcodeBookmark \\b", field.GetFieldCode());

// Закладка, на которую ссылается поле ШТРИХ-КОД в свойстве PostalAddress
// не должен содержать ничего, кроме действительного почтового индекса.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("BarcodeBookmark");
builder.Writeln("968877");
builder.EndBookmark("BarcodeBookmark");

doc.Save(ArtifactsDir + "Field.BARCODE.docx");
```

### Смотрите также

* class [FieldBarcode](../)
* пространство имен [Aspose.Words.Fields](../../fieldbarcode/)
* сборка [Aspose.Words](../../../)


