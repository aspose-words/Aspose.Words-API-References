---
title: "Aspose::Words::Fields::FieldListNum::get_ListName método"
linktitle: "get_ListName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldListNum::get_ListName método. Obtiene o establece el nombre de la definición de numeración abstracta utilizada para la numeración en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.fields/fieldlistnum/get_listname/
---
## FieldListNum::get_ListName method


Obtiene o establece el nombre de la definición de numeración abstracta utilizada para la numeración.

```cpp
System::String Aspose::Words::Fields::FieldListNum::get_ListName()
```


## Ejemplos



Muestra cómo numerar párrafos con campos LISTNUM.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Los campos LISTNUM muestran un número que se incrementa en cada campo LISTNUM.
// Estos campos también tienen una variedad de opciones que nos permiten usarlos para emular listas numeradas.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));

// Las listas comienzan a contar en 1 por defecto, pero podemos establecer este número a un valor diferente, como 0.
// Este campo mostrará "0)".
field->set_StartingNumber(u"0");
builder->Writeln(u"Paragraph 1");

ASSERT_EQ(u" LISTNUM  \\s 0", field->GetFieldCode());

// Los campos LISTNUM mantienen recuentos separados para cada nivel de lista.
// Insertar un campo LISTNUM en el mismo párrafo que otro campo LISTNUM
// incrementa el nivel de la lista en lugar del recuento.
// El siguiente campo continuará el recuento que iniciamos arriba y mostrará un valor de "1" en el nivel de lista 1.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// Este campo iniciará un recuento en el nivel de lista 2. Mostrará un valor de "1".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// Este campo iniciará un recuento en el nivel de lista 3. Mostrará un valor de "1".
// Los diferentes niveles de lista tienen un formato distinto,
// por lo que estos campos combinados mostrarán un valor de "1)a)i)".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);
builder->Writeln(u"Paragraph 2");

// El siguiente campo LISTNUM que insertamos continuará el recuento en el nivel de lista
// en el que estaba el campo LISTNUM anterior.
// Podemos usar la propiedad "ListLevel" para saltar a un nivel de lista diferente.
// Si este campo LISTNUM permaneciera en el nivel de lista 3, mostraría "ii)",
// pero, como lo hemos movido al nivel de lista 2, continúa el recuento en ese nivel y muestra "b)".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListLevel(u"2");
builder->Writeln(u"Paragraph 3");

ASSERT_EQ(u" LISTNUM  \\l 2", field->GetFieldCode());

// Podemos establecer la propiedad ListName para que el campo emule un tipo de campo AUTONUM diferente.
// "NumberDefault" emula AUTONUM, "OutlineDefault" emula AUTONUMOUT,
// y "LegalDefault" emula campos AUTONUMLGL.
// El nombre de lista "OutlineDefault" con 1 como número inicial resultará en mostrar "I.".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_StartingNumber(u"1");
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 4");

ASSERT_TRUE(field->get_HasListName());
ASSERT_EQ(u" LISTNUM  OutlineDefault \\s 1", field->GetFieldCode());

// El ListName no se mantiene del campo anterior, por lo que necesitaremos establecerlo para cada campo nuevo.
// Este campo continúa la cuenta con un nombre de lista diferente y muestra "II.".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 5");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.LISTNUM.docx");
```

## Ver también

* Class [FieldListNum](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
