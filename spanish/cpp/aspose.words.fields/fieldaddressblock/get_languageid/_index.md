---
title: "Método Aspose::Words::Fields::FieldAddressBlock::get_LanguageId"
linktitle: "get_LanguageId"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::FieldAddressBlock::get_LanguageId. Obtiene o establece el ID de idioma utilizado para formatear la dirección en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.fields/fieldaddressblock/get_languageid/
---
## FieldAddressBlock::get_LanguageId method


Obtiene o establece el ID de idioma utilizado para formatear la dirección.

```cpp
System::String Aspose::Words::Fields::FieldAddressBlock::get_LanguageId()
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
