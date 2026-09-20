---
title: "Aspose::Words::Fields::FieldXE clase"
linktitle: "FieldXE"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldXE clase. Implementa el campo XE. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 111000
url: /es/cpp/aspose.words.fields/fieldxe/
---
## FieldXE class


Implementa el campo XE. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldXE : public Aspose::Words::Fields::Field,
                public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Obtiene el texto que representa el resultado del campo mostrado. |
| [get_End](../field/get_end/)() const | Obtiene el nodo que representa el final del campo. |
| [get_EntryType](./get_entrytype/)() | Obtiene o establece un tipo de entrada de índice. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_Format](../field/get_format/)() | Obtiene un objeto [FieldFormat](../fieldformat/) que proporciona acceso tipado al formato del campo. |
| [get_IsBold](./get_isbold/)() | Obtiene o establece si se debe aplicar formato en negrita al número de página de la entrada. |
| [get_IsDirty](../field/get_isdirty/)() | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [get_IsItalic](./get_isitalic/)() | Obtiene o establece si se debe aplicar formato en cursiva al número de página de la entrada. |
| [get_IsLocked](../field/get_islocked/)() | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [get_LocaleId](../field/get_localeid/)() | Obtiene o establece el LCID del campo. |
| [get_PageNumberReplacement](./get_pagenumberreplacement/)() | Obtiene o establece el texto usado en lugar de un número de página. |
| [get_PageRangeBookmarkName](./get_pagerangebookmarkname/)() | Obtiene o establece el nombre del marcador que indica un rango de páginas que se inserta como el número de página de la entrada. |
| [get_Result](../field/get_result/)() | Obtiene o establece el texto que está entre el separador del campo y el final del campo. |
| [get_Separator](../field/get_separator/)() | Obtiene el nodo que representa el separador del campo. Puede ser **null**. |
| [get_Start](../field/get_start/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_Text](./get_text/)() | Obtiene o establece el texto de la entrada. |
| virtual [get_Type](../field/get_type/)() const | Obtiene el tipo de campo de Microsoft Word. |
| [get_Yomi](./get_yomi/)() | Obtiene o establece el yomi (primer carácter fonético para ordenar índices) de la entrada de índice. |
| [GetFieldCode](../field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado de los campos secundarios. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve **null**. |
| [set_EntryType](./set_entrytype/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldXE::get_EntryType](./get_entrytype/). |
| [set_IsBold](./set_isbold/)(bool) | Método set para [Aspose::Words::Fields::FieldXE::get_IsBold](./get_isbold/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsItalic](./set_isitalic/)(bool) | Método set para [Aspose::Words::Fields::FieldXE::get_IsItalic](./get_isitalic/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Método set para [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumberReplacement](./set_pagenumberreplacement/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldXE::get_PageNumberReplacement](./get_pagenumberreplacement/). |
| [set_PageRangeBookmarkName](./set_pagerangebookmarkname/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldXE::get_PageRangeBookmarkName](./get_pagerangebookmarkname/). |
| [set_Result](../field/set_result/)(const System::String\&) | Método set para [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_Text](./set_text/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldXE::get_Text](./get_text/). |
| [set_Yomi](./set_yomi/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldXE::get_Yomi](./get_yomi/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Ejecuta la desvinculación del campo. |
| [Update](../field/update/)() | Ejecuta la actualización del campo. Lanza una excepción si el campo ya está siendo actualizado. |
| [Update](../field/update/)(bool) | Realiza una actualización de campo. Lanza una excepción si el campo ya está siendo actualizado. |

## Ejemplos



Muestra cómo crear un campo INDEX y luego usar campos XE para poblarlo con entradas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea un campo INDEX que mostrará una entrada por cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad Text del campo XE en el lado izquierdo
// y la página que contiene el campo XE a la derecha.
// Si los campos XE tienen el mismo valor en su propiedad "Text",
// el campo INDEX los agrupará en una sola entrada.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Configura el campo INDEX para que solo muestre los campos XE que estén dentro de los límites
// de un marcador llamado "MainBookmark", y cuyas propiedades "EntryType" tengan un valor de "A".
// Para los campos INDEX y XE, la propiedad "EntryType" solo utiliza el primer carácter de su valor de cadena.
index->set_BookmarkName(u"MainBookmark");
index->set_EntryType(u"A");

ASSERT_EQ(u" INDEX  \\b MainBookmark \\f A", index->GetFieldCode());

// En una página nueva, inicia el marcador con un nombre que coincida con el valor
// de la propiedad "BookmarkName" del campo INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MainBookmark");

// El campo INDEX capturará esta entrada porque está dentro del marcador,
// y su tipo de entrada también coincide con el tipo de entrada del campo INDEX.
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 1");
indexEntry->set_EntryType(u"A");

ASSERT_EQ(u" XE  \"Index entry 1\" \\f A", indexEntry->GetFieldCode());

// Inserta un campo XE que no aparecerá en el INDEX porque los tipos de entrada no coinciden.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 2");
indexEntry->set_EntryType(u"B");

// Finaliza el marcador e inserta un campo XE después.
// Es del mismo tipo que el campo INDEX, pero no aparecerá
// ya que está fuera de los límites del marcador.
builder->EndBookmark(u"MainBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 3");
indexEntry->set_EntryType(u"A");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Filtering.docx");
```


Muestra cómo poblar un campo INDEX con entradas usando campos XE y también modificar su apariencia.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea un campo INDEX que mostrará una entrada por cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad Text del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// Si los campos XE tienen el mismo valor en su propiedad "Text",
// el campo INDEX los agrupará en una sola entrada.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));
index->set_LanguageId(u"1033");

// Establecer el valor de esta propiedad a "A" agrupará todas las entradas por su primera letra,
// y colocará esa letra en mayúsculas sobre cada grupo.
index->set_Heading(u"A");

// Configure la tabla creada por el campo INDEX para que abarque 2 columnas.
index->set_NumberOfColumns(u"2");

// Configure cualquier entrada con letras iniciales fuera del rango de caracteres "a-c" para que se omita.
index->set_LetterRange(u"a-c");

ASSERT_EQ(u" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index->GetFieldCode());

// Los siguientes dos campos XE aparecerán bajo el encabezado "A",
// con sus respectivos estilos de texto también aplicados a sus números de página.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apple");
indexEntry->set_IsItalic(true);

ASSERT_EQ(u" XE  Apple \\i", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apricot");
indexEntry->set_IsBold(true);

ASSERT_EQ(u" XE  Apricot \\b", indexEntry->GetFieldCode());

// Los dos siguientes campos XE estarán bajo los encabezados "B" y "C" en el índice de contenidos de los campos INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Banana");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cherry");

// Los campos INDEX ordenan todas las entradas alfabéticamente, por lo que esta entrada aparecerá bajo "A" con las otras dos.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Avocado");

// Esta entrada no aparecerá porque comienza con la letra "D",
// que está fuera del rango de caracteres "a-c" que define la propiedad LetterRange del campo INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Durian");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Formatting.docx");
```

## Ver también

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
