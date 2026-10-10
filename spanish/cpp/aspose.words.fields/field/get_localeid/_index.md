---
title: "Aspose::Words::Fields::Field::get_LocaleId method"
linktitle: "get_LocaleId"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::Field::get_LocaleId method. Obtiene o establece el LCID del campo en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.fields/field/get_localeid/
---
## Field::get_LocaleId method


Obtiene o establece el LCID del campo.

```cpp
int32_t Aspose::Words::Fields::Field::get_LocaleId()
```


## Ejemplos



Muestra cómo insertar un campo y trabajar con su configuración regional.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte un campo DATE y luego imprima la fecha que mostrará.
// La cultura actual de su hilo determina el formato de la fecha.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE");
std::cout << System::String::Format(u"Today's date, as displayed in the \"{0}\" culture: {1}", System::Globalization::CultureInfo::get_CurrentCulture()->get_EnglishName(), field->get_Result()) << std::endl;

ASSERT_EQ(1033, field->get_LocaleId());

// Cambiar la cultura de nuestro hilo afectará el resultado del campo DATE.
// Otra forma de hacer que el campo DATE muestre una fecha en una cultura diferente es usar su propiedad LocaleId.
// De esta manera nos permite evitar cambiar la cultura del hilo para obtener este efecto.
doc->get_FieldOptions()->set_FieldUpdateCultureSource(Aspose::Words::Fields::FieldUpdateCultureSource::FieldCode);
auto de = System::MakeObject<System::Globalization::CultureInfo>(u"de-DE");
field->set_LocaleId(de->get_LCID());
field->Update();

std::cout << System::String::Format(u"Today's date, as displayed according to the \"{0}\" culture: {1}", System::Globalization::CultureInfo::GetCultureInfo(field->get_LocaleId())->get_EnglishName(), field->get_Result()) << std::endl;
```

## Ver también

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
