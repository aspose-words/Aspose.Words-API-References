---
title: FieldAddressBlock.FormatAddressOnCountryOrRegion
second_title: Справочник по API Aspose.Words для .NET
description: FieldAddressBlock свойство. Получает или задает необходимость форматирования адреса в соответствии со страной/регионом получателя  как определено POSTCODE Universal Postal Union 2006.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldaddressblock/formataddressoncountryorregion/
---
## FieldAddressBlock.FormatAddressOnCountryOrRegion property

Получает или задает необходимость форматирования адреса в соответствии со страной/регионом получателя , как определено POST*CODE (Universal Postal Union 2006).

```csharp
public bool FormatAddressOnCountryOrRegion { get; set; }
```

### Примеры

Показывает, как вставить поле ADDRESSBLOCK.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldAddressBlock field = (FieldAddressBlock)builder.InsertField(FieldType.FieldAddressBlock, true);

Assert.AreEqual(" ADDRESSBLOCK ", field.GetFieldCode());

// Установка значения «2» будет включать все страны и регионы,
// если только оно не указано в свойстве ExcludedCountryOrRegionName.
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


