---
title: "Aspose::Words::Fields::FieldAddressBlock::get_FormatAddressOnCountryOrRegion método"
linktitle: "get_FormatAddressOnCountryOrRegion"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldAddressBlock::get_FormatAddressOnCountryOrRegion método. Obtiene o establece si se debe formatear la dirección de acuerdo con el país/región del destinatario según lo definido por POST*CODE (Unión Postal Universal 2006) en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.fields/fieldaddressblock/get_formataddressoncountryorregion/
---
## FieldAddressBlock::get_FormatAddressOnCountryOrRegion method


Obtiene o establece si formatear la dirección según el país/región del destinatario según lo definido por POST*CODE (Unión Postal Universal 2006).

```cpp
bool Aspose::Words::Fields::FieldAddressBlock::get_FormatAddressOnCountryOrRegion()
```


## Ejemplos



Muestra cómo insertar un campo ADDRESSBLOCK.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAddressBlock>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAddressBlock, true));

ASSERT_EQ(u" ADDRESSBLOCK ", field->GetFieldCode());

// Establecer esto en "2" incluirá todos los países y regiones,
// a menos que sea el especificado en la propiedad ExcludedCountryOrRegionName.
field->set_IncludeCountryOrRegionName(u"2");
field->set_FormatAddressOnCountryOrRegion(true);
field->set_ExcludedCountryOrRegionName(u"United States");
field->set_NameAndAddressFormat(u"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>");

// Por defecto, esta propiedad contendrá el ID de idioma del primer carácter del documento.
// Podemos establecer una cultura diferente para que el campo formatee el resultado de esta manera.
field->set_LanguageId(System::Convert::ToString(System::MakeObject<System::Globalization::CultureInfo>(u"en-US")->get_LCID()));

ASSERT_EQ(u" ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033", field->GetFieldCode());
```

## Ver también

* Class [FieldAddressBlock](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
