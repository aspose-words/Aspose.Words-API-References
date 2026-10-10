---
title: "Clase Aspose::Words::Fields::FieldToc"
linktitle: "FieldToc"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Fields::FieldToc. Implementa el campo TOC. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 105000
url: /es/cpp/aspose.words.fields/fieldtoc/
---
## FieldToc class


Implementa el campo TOC. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldToc : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Métodos

| Método | Descripción |
| --- | --- |
| [FieldToc](./fieldtoc/)() |  |
| [get_BookmarkName](./get_bookmarkname/)() | Obtiene el nombre del marcador que indica la parte del documento utilizada para crear la tabla. |
| [get_CaptionlessTableOfFiguresLabel](./get_captionlesstableoffigureslabel/)() | Obtiene o establece el nombre del identificador de secuencia utilizado al crear una tabla de figuras que no incluye la etiqueta y el número del título. |
| [get_CustomStyles](./get_customstyles/)() | Obtiene una lista de estilos, distintos de los estilos de encabezado incorporados, para incluir en la tabla de contenido. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtiene el texto que representa el resultado del campo mostrado. |
| [get_End](../field/get_end/)() const | Obtiene el nodo que representa el final del campo. |
| [get_EntryIdentifier](./get_entryidentifier/)() | Obtiene una cadena que debe coincidir con los identificadores de tipo de los campos TC que se incluyen. |
| [get_EntryLevelRange](./get_entrylevelrange/)() | Obtiene un rango de niveles de las entradas de la tabla de contenido que se incluirán. |
| [get_EntrySeparator](./get_entryseparator/)() | Obtiene una secuencia de caracteres que separan una entrada y su número de página. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_Format](../field/get_format/)() | Obtiene un objeto [FieldFormat](../fieldformat/) que proporciona acceso tipado al formato del campo. |
| [get_HeadingLevelRange](./get_headinglevelrange/)() | Obtiene un rango de niveles de encabezado para incluir. |
| [get_HideInWebLayout](./get_hideinweblayout/)() | Obtiene si se deben ocultar los guías de tabulación y los números de página en la vista de diseño web. |
| [get_InsertHyperlinks](./get_inserthyperlinks/)() | Obtiene si las entradas de la tabla de contenido deben convertirse en hipervínculos. |
| [get_IsDirty](../field/get_isdirty/)() | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [get_IsLocked](../field/get_islocked/)() | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [get_LocaleId](../field/get_localeid/)() | Obtiene o establece el LCID del campo. |
| [get_PageNumberOmittingLevelRange](./get_pagenumberomittinglevelrange/)() | Obtiene un rango de niveles de las entradas de la tabla de contenido a partir de los cuales se omiten los números de página. |
| [get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/)() | Obtiene o establece el identificador de una secuencia a la que se debe añadir un prefijo al número de página de la entrada. |
| [get_PreserveLineBreaks](./get_preservelinebreaks/)() | Obtiene si se deben conservar los caracteres de salto de línea dentro de las entradas de la tabla. |
| [get_PreserveTabs](./get_preservetabs/)() | Obtiene si se deben conservar las tabulaciones dentro de las entradas de la tabla. |
| [get_Result](../field/get_result/)() | Obtiene o establece el texto que está entre el separador del campo y el final del campo. |
| [get_Separator](../field/get_separator/)() | Obtiene el nodo que representa el separador del campo. Puede ser **null**. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Obtiene o establece la secuencia de caracteres que se usa para separar los números de secuencia y los números de página. |
| [get_Start](../field/get_start/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_TableOfFiguresLabel](./get_tableoffigureslabel/)() | Obtiene o establece el nombre del identificador de secuencia utilizado al crear una tabla de figuras. |
| virtual [get_Type](../field/get_type/)() const | Obtiene el tipo de campo de Microsoft Word. |
| [get_UseParagraphOutlineLevel](./get_useparagraphoutlinelevel/)() | Obtiene si se debe usar el nivel de esquema de párrafo aplicado. |
| [GetFieldCode](../field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado de los campos secundarios. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Establece el nombre del marcador que indica la parte del documento utilizada para crear la tabla. |
| [set_CaptionlessTableOfFiguresLabel](./set_captionlesstableoffigureslabel/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel](./get_captionlesstableoffigureslabel/). |
| [set_CustomStyles](./set_customstyles/)(const System::String\&) | Establece una lista de estilos, distintos de los estilos de encabezado incorporados, para incluir en la tabla de contenido. |
| [set_EntryIdentifier](./set_entryidentifier/)(const System::String\&) | Establece una cadena que debe coincidir con los identificadores de tipo de los campos TC que se incluyen. |
| [set_EntryLevelRange](./set_entrylevelrange/)(const System::String\&) | Establece un rango de niveles de las entradas de la tabla de contenido que se incluirán. |
| [set_EntrySeparator](./set_entryseparator/)(const System::String\&) | Establece una secuencia de caracteres que separan una entrada y su número de página. |
| [set_HeadingLevelRange](./set_headinglevelrange/)(const System::String\&) | Establece un rango de niveles de encabezado para incluir. |
| [set_HideInWebLayout](./set_hideinweblayout/)(bool) | Establece si se deben ocultar los guías de tabulación y los números de página en la vista de diseño web. |
| [set_InsertHyperlinks](./set_inserthyperlinks/)(bool) | Establece si las entradas de la tabla de contenido deben convertirse en hipervínculos. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Método set para [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumberOmittingLevelRange](./set_pagenumberomittinglevelrange/)(const System::String\&) | Establece un rango de niveles de las entradas del índice de contenido desde los cuales omitir los números de página. |
| [set_PrefixedSequenceIdentifier](./set_prefixedsequenceidentifier/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldToc::get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/). |
| [set_PreserveLineBreaks](./set_preservelinebreaks/)(bool) | Establece si se deben conservar los caracteres de salto de línea dentro de las entradas de la tabla. |
| [set_PreserveTabs](./set_preservetabs/)(bool) | Establece si se deben conservar las tabulaciones dentro de las entradas de la tabla. |
| [set_Result](../field/set_result/)(const System::String\&) | Método set para [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldToc::get_SequenceSeparator](./get_sequenceseparator/). |
| [set_TableOfFiguresLabel](./set_tableoffigureslabel/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldToc::get_TableOfFiguresLabel](./get_tableoffigureslabel/). |
| [set_UseParagraphOutlineLevel](./set_useparagraphoutlinelevel/)(bool) | Establece si se debe usar el nivel de esquema de párrafo aplicado. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Ejecuta la desvinculación del campo. |
| [Update](../field/update/)() | Ejecuta la actualización del campo. Lanza una excepción si el campo ya está siendo actualizado. |
| [Update](../field/update/)(bool) | Realiza una actualización de campo. Lanza una excepción si el campo ya está siendo actualizado. |
| [UpdatePageNumbers](./updatepagenumbers/)() | Actualiza los números de página de los elementos en este índice de contenido. |

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

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
