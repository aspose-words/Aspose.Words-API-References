---
title: FieldBarcode.PostalAddress
linktitle: PostalAddress
articleTitle: PostalAddress
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldBarcode PostalAddress, чтобы легко управлять почтовыми адресами для генерации штрихкодов и ссылок на закладки. Упростите свой рабочий процесс сегодня!
type: docs
weight: 50
url: /ru/net/aspose.words.fields/fieldbarcode/postaladdress/
---
## FieldBarcode.PostalAddress property

Возвращает или задает почтовый адрес, используемый для генерации штрих-кода, или имя закладки, которая ссылается на него.

```csharp
public string PostalAddress { get; set; }
```

## Примеры

Показывает, как использовать поле ШТРИХ-КОД для отображения почтовых индексов США в виде штрих-кода.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Ниже приведены два способа использования полей BARCODE для отображения пользовательских значений в виде штрихкодов.
// 1 — Сохраните значение, которое будет отображаться в штрих-коде, в свойстве PostalAddress:
FieldBarcode field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);

// Это значение должно быть действительным почтовым индексом.
field.PostalAddress = "96801";
field.IsUSPostalAddress = true;
field.FacingIdentificationMark = "C";

Assert.AreEqual(" BARCODE  96801 \\u \\f C", field.GetFieldCode());

builder.InsertBreak(BreakType.LineBreak);

// 2 — Ссылка на закладку, в которой хранится значение, которое будет отображать этот штрих-код:
field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);
field.PostalAddress = "BarcodeBookmark";
field.IsBookmark = true;

Assert.AreEqual(" BARCODE  BarcodeBookmark \\b", field.GetFieldCode());

// Закладка, на которую ссылается поле BARCODE в своем свойстве PostalAddress
// не должны содержать ничего, кроме действительного почтового индекса.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("BarcodeBookmark");
builder.Writeln("968877");
builder.EndBookmark("BarcodeBookmark");

doc.Save(ArtifactsDir + "Field.BARCODE.docx");
```

### Смотрите также

* class [FieldBarcode](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
