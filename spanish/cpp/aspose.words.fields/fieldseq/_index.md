---
title: "Clase Aspose::Words::Fields::FieldSeq"
linktitle: "FieldSeq"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Fields::FieldSeq. Implementa el campo SEQ. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 91000
url: /es/cpp/aspose.words.fields/fieldseq/
---
## FieldSeq class


Implementa el campo SEQ. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldSeq : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Obtiene o establece un nombre de marcador que se refiere a un elemento en otra parte del documento en lugar de la ubicación actual. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtiene el texto que representa el resultado del campo mostrado. |
| [get_End](../field/get_end/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_Format](../field/get_format/)() | Obtiene un objeto [FieldFormat](../fieldformat/) que proporciona acceso tipado al formato del campo. |
| [get_InsertNextNumber](./get_insertnextnumber/)() | Obtiene o establece si se debe insertar el siguiente número de secuencia para el elemento especificado. |
| [get_IsDirty](../field/get_isdirty/)() | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [get_IsLocked](../field/get_islocked/)() | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [get_LocaleId](../field/get_localeid/)() | Obtiene o establece el LCID del campo. |
| [get_ResetHeadingLevel](./get_resetheadinglevel/)() | Obtiene o establece un número entero que representa un nivel de encabezado al que restablecer el número de secuencia. Devuelve -1 si el número está ausente. |
| [get_ResetNumber](./get_resetnumber/)() | Obtiene o establece un número entero al que restablecer el número de secuencia. Devuelve -1 si el número está ausente. |
| [get_Result](../field/get_result/)() | Obtiene o establece el texto que está entre el separador del campo y el final del campo. |
| [get_Separator](../field/get_separator/)() | Obtiene el nodo que representa el separador del campo. Puede ser **null**. |
| [get_SequenceIdentifier](./get_sequenceidentifier/)() | Obtiene o establece el nombre asignado a la serie de elementos que deben numerarse. |
| [get_Start](../field/get_start/)() const | Obtiene el nodo que representa el inicio del campo. |
| virtual [get_Type](../field/get_type/)() const | Obtiene el tipo de campo de Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado de los campos secundarios. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Establecedor para [Aspose::Words::Fields::FieldSeq::get_BookmarkName](./get_bookmarkname/). |
| [set_InsertNextNumber](./set_insertnextnumber/)(bool) | Establecedor para [Aspose::Words::Fields::FieldSeq::get_InsertNextNumber](./get_insertnextnumber/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Método set para [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_ResetHeadingLevel](./set_resetheadinglevel/)(const System::String\&) | Establecedor para [Aspose::Words::Fields::FieldSeq::get_ResetHeadingLevel](./get_resetheadinglevel/). |
| [set_ResetNumber](./set_resetnumber/)(const System::String\&) | Establecedor para [Aspose::Words::Fields::FieldSeq::get_ResetNumber](./get_resetnumber/). |
| [set_Result](../field/set_result/)(const System::String\&) | Método set para [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceIdentifier](./set_sequenceidentifier/)(const System::String\&) | Establecedor para [Aspose::Words::Fields::FieldSeq::get_SequenceIdentifier](./get_sequenceidentifier/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Ejecuta la desvinculación del campo. |
| [Update](../field/update/)() | Ejecuta la actualización del campo. Lanza una excepción si el campo ya está siendo actualizado. |
| [Update](../field/update/)(bool) | Realiza una actualización de campo. Lanza una excepción si el campo ya está siendo actualizado. |

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


Muestra la creación de numeración usando campos SEQ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Los campos SEQ muestran un recuento que se incrementa en cada campo SEQ.
// Estos campos también mantienen recuentos separados para cada secuencia nombrada única
// identificado por la propiedad "SequenceIdentifier" del campo SEQ.
// Inserte un campo SEQ que mostrará el valor de recuento actual de "MySequence",
// después de usar la propiedad "ResetNumber" para establecerlo en 100.
builder->Write(u"#");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetNumber(u"100");
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\r 100", fieldSeq->GetFieldCode());
ASSERT_EQ(u"100", fieldSeq->get_Result());

// Muestre el siguiente número en esta secuencia con otro campo SEQ.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->Update();

ASSERT_EQ(u"101", fieldSeq->get_Result());

// Inserte un encabezado de nivel 1.
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"This level 1 heading will reset MySequence to 1");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));

// Inserte otro campo SEQ de la misma secuencia y configúrelo para restablecer el recuento en cada encabezado con 1.
builder->Write(u"\n#");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetHeadingLevel(u"1");
fieldSeq->Update();

// El encabezado anterior es un encabezado de nivel 1, por lo que el recuento de esta secuencia se restablece a 1.
ASSERT_EQ(u" SEQ  MySequence \\s 1", fieldSeq->GetFieldCode());
ASSERT_EQ(u"1", fieldSeq->get_Result());

// Pase al siguiente número de esta secuencia.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_InsertNextNumber(true);
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\n", fieldSeq->GetFieldCode());
ASSERT_EQ(u"2", fieldSeq->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.ResetNumbering.docx");
```


Muestra cómo combinar la tabla de contenido y los campos de secuencia.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Un campo TOC puede crear una entrada en su tabla de contenido para cada campo SEQ encontrado en el documento.
// Cada entrada contiene el párrafo que contiene el campo SEQ,
// y el número de página en el que aparece el campo.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// Configure este campo TOC para que tenga una propiedad SequenceIdentifier con el valor "MySequence".
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// Configure este campo TOC para que solo capture campos SEQ que estén dentro de los límites de un marcador
// llamado "TOCBookmark".
fieldToc->set_BookmarkName(u"TOCBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

ASSERT_EQ(u" TOC  \\c MySequence \\b TOCBookmark", fieldToc->GetFieldCode());

// Los campos SEQ muestran un recuento que se incrementa en cada campo SEQ.
// Estos campos también mantienen recuentos separados para cada secuencia nombrada única
// identificado por la propiedad "SequenceIdentifier" del campo SEQ.
// Inserte un campo SEQ que tenga un identificador de secuencia que coincida con el de TOC
// propiedad TableOfFiguresLabel. Este campo no creará una entrada en el TOC ya que está fuera
// de los límites del marcador designados por "BookmarkName".
builder->Write(u"MySequence #");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will not show up in the TOC because it is outside of the bookmark.");

builder->StartBookmark(u"TOCBookmark");

// La secuencia de este campo SEQ coincide con la propiedad "TableOfFiguresLabel" del TOC y está dentro de los límites del marcador.
// El párrafo que contiene este campo aparecerá en el TOC como una entrada.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will show up in the TOC next to the entry for the above caption.");

// La secuencia de este campo SEQ no coincide con la propiedad "TableOfFiguresLabel" del TOC,
// y está dentro de los límites del marcador. Su párrafo no aparecerá en el TOC como una entrada.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"OtherSequence");
builder->Writeln(u", will not show up in the TOC because it's from a different sequence identifier.");

// La secuencia de este campo SEQ coincide con la propiedad "TableOfFiguresLabel" del TOC y está dentro de los límites del marcador.
// Este campo también hace referencia a otro marcador. El contenido de ese marcador aparecerá en la entrada del TOC para este campo SEQ.
// El propio campo SEQ no mostrará el contenido de ese marcador.
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_BookmarkName(u"SEQBookmark");
ASSERT_EQ(u" SEQ  MySequence SEQBookmark", fieldSeq->GetFieldCode());

// Cree un marcador con contenido que aparecerá en la entrada del TOC debido a que el campo SEQ anterior lo referencia.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"SEQBookmark");
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", text from inside SEQBookmark.");
builder->EndBookmark(u"SEQBookmark");

builder->EndBookmark(u"TOCBookmark");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.Bookmark.docx");
```

## Ver también

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
