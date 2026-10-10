---
title: "Método Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat"
linktitle: "get_UseInvariantCultureNumberFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat. Obtiene o establece el valor que indica si el formato numérico se analiza usando la cultura invariante o no en C++."
type: docs
weight: 21000
url: /es/cpp/aspose.words.fields/fieldoptions/get_useinvariantculturenumberformat/
---
## FieldOptions::get_UseInvariantCultureNumberFormat method


Obtiene o establece el valor que indica si el formato numérico se analiza usando la cultura invariante o no.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat() const
```

## Observaciones


Cuando esta propiedad se establece en **true**, el formato numérico se toma de una cultura invariante.

Cuando esta propiedad se establece en **false**, el formato numérico se toma de la cultura del hilo actual.

El valor predeterminado es **false**.

## Ejemplos



Muestra cómo formatear números según la cultura invariante.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::Threading::Thread::get_CurrentThread()->set_CurrentCulture(System::MakeObject<System::Globalization::CultureInfo>(u"de-DE"));
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" = 1234567,89 \\# $#,###,###.##");
field->Update();

// A veces, los campos pueden no formatear sus números correctamente bajo ciertas culturas.
ASSERT_FALSE(doc->get_FieldOptions()->get_UseInvariantCultureNumberFormat());
ASSERT_EQ(u"$1.234.567,89 ,     ", field->get_Result());

// Para solucionar esto, podríamos cambiar la cultura de todo el hilo.
// Otra forma de solucionar esto es establecer esta bandera,
// lo que hace que todos los campos usen la cultura invariante al formatear números.
// De esta manera nos permite evitar cambiar la cultura de todo el hilo.
doc->get_FieldOptions()->set_UseInvariantCultureNumberFormat(true);
field->Update();
ASSERT_EQ(u"$1.234.567,89", field->get_Result());
```

## Ver también

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
