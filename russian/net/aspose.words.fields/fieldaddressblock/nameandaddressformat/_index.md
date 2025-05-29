---
title: FieldAddressBlock.NameAndAddressFormat
linktitle: NameAndAddressFormat
articleTitle: NameAndAddressFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство NameAndAddressFormat объекта FieldAddressBlock, чтобы легко настраивать форматы имени и адреса для улучшенного управления данными.
type: docs
weight: 60
url: /ru/net/aspose.words.fields/fieldaddressblock/nameandaddressformat/
---
## FieldAddressBlock.NameAndAddressFormat property

Получает или задает формат имени и адреса.

```csharp
public string NameAndAddressFormat { get; set; }
```

## Примеры

Показывает, как вставить поле ADDRESSBLOCK.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldAddressBlock field = (FieldAddressBlock)builder.InsertField(FieldType.FieldAddressBlock, true);

Assert.AreEqual(" ADDRESSBLOCK ", field.GetFieldCode());

// Если установить значение "2", будут включены все страны и регионы,
// если только это не тот, который указан в свойстве ExcludedCountryOrRegionName.
field.IncludeCountryOrRegionName = "2";
field.FormatAddressOnCountryOrRegion = true;
field.ExcludedCountryOrRegionName = "United States";
field.NameAndAddressFormat = "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>";

// По умолчанию это свойство будет содержать идентификатор языка первого символа документа.
// Мы можем задать другую культуру для поля, чтобы отформатировать результат следующим образом.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(
    " ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033",
    field.GetFieldCode());
```

### Смотрите также

* class [FieldAddressBlock](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
