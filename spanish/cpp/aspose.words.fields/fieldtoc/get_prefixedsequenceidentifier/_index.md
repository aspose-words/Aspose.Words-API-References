---
title: "Aspose::Words::Fields::FieldToc::get_PrefixedSequenceIdentifier método"
linktitle: "get_PrefixedSequenceIdentifier"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldToc::get_PrefixedSequenceIdentifier método. Obtiene o establece el identificador de una secuencia para la cual se debe agregar un prefijo al número de página de la entrada en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words.fields/fieldtoc/get_prefixedsequenceidentifier/
---
## FieldToc::get_PrefixedSequenceIdentifier method


Obtiene o establece el identificador de una secuencia a la que se debe añadir un prefijo al número de página de la entrada.

```cpp
System::String Aspose::Words::Fields::FieldToc::get_PrefixedSequenceIdentifier()
```


## Ejemplos



Muestra cómo rellenar un campo TOC con entradas usando campos SEQ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Un campo TOC puede crear una entrada en su tabla de contenido para cada campo SEQ encontrado en el documento.
// Cada entrada contiene el párrafo que incluye el campo SEQ y el número de página en el que aparece el campo.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// Los campos SEQ muestran un recuento que se incrementa en cada campo SEQ.
// Estos campos también mantienen recuentos separados para cada secuencia nombrada única
// identificado por la propiedad "SequenceIdentifier" del campo SEQ.
// Utilice la propiedad "TableOfFiguresLabel" para nombrar una secuencia principal para el TOC.
// Ahora, este TOC solo creará entradas a partir de campos SEQ cuya "SequenceIdentifier" esté establecida en "MySequence".
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// Podemos nombrar otra secuencia de campo SEQ en la propiedad "PrefixedSequenceIdentifier".
// Los campos SEQ de esta secuencia de prefijo no crearán entradas en el TOC.
// Cada entrada del TOC creada a partir de un campo SEQ de secuencia principal ahora también mostrará el recuento que
// la secuencia de prefijo está actualmente en el campo SEQ de secuencia primaria que generó la entrada.
fieldToc->set_PrefixedSequenceIdentifier(u"PrefixSequence");

// Cada entrada del TOC mostrará el recuento de la secuencia de prefijo inmediatamente a la izquierda
// del número de página en la que aparece el campo SEQ de secuencia principal.
// Podemos especificar un separador personalizado que aparecerá entre estos dos números.
fieldToc->set_SequenceSeparator(u">");

ASSERT_EQ(u" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Hay dos formas de usar campos SEQ para rellenar este TOC.
// 1 -  Insertar un campo SEQ que pertenece a la secuencia de prefijo del TOC:
// Este campo incrementará el recuento de la secuencia SEQ para "PrefixSequence" en 1.
// Dado que este campo no pertenece a la secuencia principal identificada
// por la propiedad "TableOfFiguresLabel" del TOC, no aparecerá como una entrada.
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();

ASSERT_EQ(u" SEQ  PrefixSequence", fieldSeq->GetFieldCode());

// 2 -  Insertar un campo SEQ que pertenece a la secuencia principal del TOC:
// Este campo SEQ creará una entrada en el TOC.
// La entrada del TOC contendrá el párrafo en el que se encuentra el campo SEQ y el número de página en que aparece.
// Esta entrada también mostrará el recuento en el que se encuentra actualmente la secuencia de prefijo,
// separado del número de página por el valor de la propiedad SeqenceSeparator del TOC.
// El recuento de "PrefixSequence" está en 1, este campo SEQ de secuencia principal está en la página 2,
// y el separador es ">", por lo que la entrada mostrará "1>2".
builder->Write(u"First TOC entry, MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", fieldSeq->GetFieldCode());

// Inserte una página, avance la secuencia de prefijo en 2 e inserte un campo SEQ para crear una entrada del TOC después.
// La secuencia de prefijo está ahora en 2, y el campo SEQ de secuencia principal está en la página 3,
// por lo que la entrada del TOC mostrará "2>3" en su recuento de página.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
builder->Write(u"Second TOC entry, MySequence #");
fieldSeq->set_SequenceIdentifier(u"MySequence");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TOC.SEQ.docx");
```

## Ver también

* Class [FieldToc](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
