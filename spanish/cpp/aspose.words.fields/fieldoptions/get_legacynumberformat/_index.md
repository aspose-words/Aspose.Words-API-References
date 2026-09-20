---
title: "Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat método"
linktitle: "get_LegacyNumberFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat method. Obtiene o establece el valor que indica si el formato numérico heredado (anterior a AW 13.10) para los campos está habilitado o no en C++."
type: docs
weight: 16000
url: /es/cpp/aspose.words.fields/fieldoptions/get_legacynumberformat/
---
## FieldOptions::get_LegacyNumberFormat method


Obtiene o establece el valor que indica si el formato numérico heredado (anterior a AW 13.10) para los campos está habilitado o no.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat() const
```

## Observaciones


Cuando esta propiedad se establece en **true**, el símbolo de plantilla "#" funciona como en .net: Reemplaza el signo de libra por el dígito correspondiente si está presente; de lo contrario, no aparecen símbolos en la cadena resultante.

Cuando esta propiedad se establece en **false**, el símbolo de plantilla "#" funciona como MS Word: Este elemento de formato especifica los lugares numéricos requeridos para mostrarse en el resultado. Si el resultado no incluye un dígito en ese lugar, MS Word muestra un espacio. Por ejemplo, { = 9 + 6 \\# $### } muestra $ 15.

El valor predeterminado es **false**.

## Ejemplos



Muestra cómo habilitar el formato numérico heredado para los campos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3 \\# $##");

ASSERT_EQ(u"$ 5", field->get_Result());

doc->get_FieldOptions()->set_LegacyNumberFormat(true);
field->Update();

ASSERT_EQ(u"$5", field->get_Result());
```

## Ver también

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
