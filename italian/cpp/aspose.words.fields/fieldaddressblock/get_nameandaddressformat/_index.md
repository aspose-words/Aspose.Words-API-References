---
title: "Aspose::Words::Fields::FieldAddressBlock::get_NameAndAddressFormat metodo"
linktitle: "get_NameAndAddressFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldAddressBlock::get_NameAndAddressFormat metodo. Ottiene o imposta il formato nome e indirizzo in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.fields/fieldaddressblock/get_nameandaddressformat/
---
## FieldAddressBlock::get_NameAndAddressFormat method


Ottiene o imposta il formato del nome e dell'indirizzo.

```cpp
System::String Aspose::Words::Fields::FieldAddressBlock::get_NameAndAddressFormat()
```


## Esempi



Mostra come inserire un campo ADDRESSBLOCK.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAddressBlock>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAddressBlock, true));

ASSERT_EQ(u" ADDRESSBLOCK ", field->GetFieldCode());

// Impostando questo su "2" includerà tutti i paesi e le regioni,
// a meno che non sia quello specificato nella proprietà ExcludedCountryOrRegionName.
field->set_IncludeCountryOrRegionName(u"2");
field->set_FormatAddressOnCountryOrRegion(true);
field->set_ExcludedCountryOrRegionName(u"United States");
field->set_NameAndAddressFormat(u"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>");

// Per impostazione predefinita, questa proprietà conterrà l'ID lingua del primo carattere del documento.
// Possiamo impostare una cultura diversa per il campo per formattare il risultato in questo modo.
field->set_LanguageId(System::Convert::ToString(System::MakeObject<System::Globalization::CultureInfo>(u"en-US")->get_LCID()));

ASSERT_EQ(u" ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033", field->GetFieldCode());
```

## Vedi anche

* Class [FieldAddressBlock](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
