---
title: FieldAddressBlock.LanguageId
linktitle: LanguageId
articleTitle: LanguageId
second_title: Aspose.Words для .NET
description: Управляйте форматированием адреса без усилий с помощью свойства FieldAddressBlock LanguageId. Установите или получите идентификатор языка для бесшовной локализации.
type: docs
weight: 50
url: /ru/net/aspose.words.fields/fieldaddressblock/languageid/
---
## FieldAddressBlock.LanguageId property

Возвращает или задает идентификатор языка, используемый для форматирования адреса.

```csharp
public string LanguageId { get; set; }
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
