---
title: FieldAddressBlock.ExcludedCountryOrRegionName
second_title: Справочник по API Aspose.Words для .NET
description: FieldAddressBlock свойство. Получает или задает название исключенной страны/региона.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldaddressblock/excludedcountryorregionname/
---
## FieldAddressBlock.ExcludedCountryOrRegionName property

Получает или задает название исключенной страны/региона.

```csharp
public string ExcludedCountryOrRegionName { get; set; }
```

### Примеры

Показывает, как вставить поле ADDRESSBLOCK.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldAddressBlock field = (FieldAddressBlock)builder.InsertField(FieldType.FieldAddressBlock, true);

Assert.AreEqual(" ADDRESSBLOCK ", field.GetFieldCode());

// Установка этого параметра на "2" будет включать все страны и регионы,
// если только он не указан в свойстве ExcludedCountryOrRegionName.
field.IncludeCountryOrRegionName = "2";
field.FormatAddressOnCountryOrRegion = true;
field.ExcludedCountryOrRegionName = "United States";
field.NameAndAddressFormat = "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>";

// По умолчанию это свойство будет содержать идентификатор языка первого символа документа.
// Мы можем установить другую культуру для поля, чтобы отформатировать результат следующим образом.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(
    " ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033",
    field.GetFieldCode());
```

### Смотрите также

* class [FieldAddressBlock](../)
* пространство имен [Aspose.Words.Fields](../../fieldaddressblock/)
* сборка [Aspose.Words](../../../)


