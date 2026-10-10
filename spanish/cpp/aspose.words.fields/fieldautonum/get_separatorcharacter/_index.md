---
title: "Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter método"
linktitle: "get_SeparatorCharacter"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter método. Obtiene o establece el carácter separador que se usará en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldautonum/get_separatorcharacter/
---
## FieldAutoNum::get_SeparatorCharacter method


Obtiene o establece el carácter separador que se utilizará.

```cpp
System::String Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter()
```


## Ejemplos



Muestra cómo numerar párrafos usando campos autonum.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Cada campo AUTONUM muestra el valor actual de un recuento continuo de campos AUTONUM,
// permitiéndonos numerar automáticamente los elementos como en una lista numerada.
// Este campo mostrará el número "1.".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAutoNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNum, true));
builder->Writeln(u"\tParagraph 1.");

ASSERT_EQ(u" AUTONUM ", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldAutoNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNum, true));
builder->Writeln(u"\tParagraph 2.");

// El carácter separador, que aparece en el resultado del campo inmediatamente después del número, es un punto por defecto.
// Si dejamos esta propiedad nula, nuestro segundo campo AUTONUM mostrará "2." en el documento.
ASSERT_TRUE(System::TestTools::IsNull(field->get_SeparatorCharacter()));

// Podemos establecer esta propiedad para aplicar el primer carácter de su cadena como el nuevo carácter separador.
// En este caso, nuestro campo AUTONUM ahora mostrará "2:".
field->set_SeparatorCharacter(u":");

ASSERT_EQ(u" AUTONUM  \\s :", field->GetFieldCode());

doc->Save(get_ArtifactsDir() + u"Field.AUTONUM.docx");
```

## Ver también

* Class [FieldAutoNum](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
