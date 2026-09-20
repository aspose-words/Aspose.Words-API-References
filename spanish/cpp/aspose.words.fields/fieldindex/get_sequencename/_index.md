---
title: "Método Aspose::Words::Fields::FieldIndex::get_SequenceName"
linktitle: "get_SequenceName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::FieldIndex::get_SequenceName. Obtiene o establece el nombre de una secuencia cuyo número se incluye con el número de página en C++."
type: docs
weight: 15000
url: /es/cpp/aspose.words.fields/fieldindex/get_sequencename/
---
## FieldIndex::get_SequenceName method


Obtiene o establece el nombre de una secuencia cuyo número se incluye con el número de página.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_SequenceName()
```


## Ejemplos



Muestra cómo dividir un documento en partes combinando los campos INDEX y SEQ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea un campo INDEX que mostrará una entrada por cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad Text del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// Si los campos XE tienen el mismo valor en su propiedad "Text",
// el campo INDEX los agrupará en una sola entrada.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// En la propiedad SequenceName, nombre una secuencia de campo SEQ. Cada entrada de este campo INDEX ahora también mostrará
// el número en el que se encuentra el recuento de la secuencia en la ubicación del campo XE que creó esta entrada.
index->set_SequenceName(u"MySequence");

// Establezca texto que rodeará la secuencia y los números de página para explicar su significado al usuario.
// Una entrada creada con esta configuración mostrará algo como "MySequence at 1 on page 1" en su número de página.
// PageNumberSeparator y SequenceSeparator no pueden tener más de 15 caracteres.
index->set_PageNumberSeparator(u"\tMySequence at ");
index->set_SequenceSeparator(u" on page ");
ASSERT_TRUE(index->get_HasSequenceName());

ASSERT_EQ(u" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index->GetFieldCode());

// Los campos SEQ muestran un recuento que se incrementa en cada campo SEQ.
// Estos campos también mantienen recuentos separados para cada secuencia nombrada única
// identificado por la propiedad "SequenceIdentifier" del campo SEQ.
// Inserte un campo SEQ que mueva la secuencia "MySequence" a 1.
// Este campo no es diferente del texto normal del documento. No aparecerá en la tabla de contenido de un campo INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", sequenceField->GetFieldCode());

// Inserte un campo XE que creará una entrada en el campo INDEX.
// Dado que "MySequence" está en 1 y este campo XE está en la página 2, junto con los separadores personalizados que definimos arriba,
// La entrada INDEX de este campo mostrará "Cat" en el lado izquierdo y "MySequence at 1 on page 2" en el derecho.
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cat");

ASSERT_EQ(u" XE  Cat", indexEntry->GetFieldCode());

// Inserte un salto de página y use campos SEQ para avanzar "MySequence" a 3.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");
sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");

// Inserte un campo XE con la misma propiedad Text que el anterior.
// La entrada INDEX agrupará los campos XE con valores coincidentes en la propiedad "Text".
// en una sola entrada en lugar de crear una entrada para cada campo XE.
// Dado que estamos en la página 2 con "MySequence" en 3, ", 3 on page 3" se añadirá a la misma entrada INDEX que arriba.
// La parte del número de página de esa entrada INDEX ahora mostrará "MySequence at 1 on page 2, 3 on page 3".
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cat");

// Inserte un campo XE con un nuevo y único valor de la propiedad Text.
// Esto añadirá una nueva entrada, con MySequence en 3 en la página 4.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Dog");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Sequence.docx");
```

## Ver también

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
