---
title: "Método Aspose::Words::Fields::FieldSeq::get_BookmarkName"
linktitle: "get_BookmarkName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::FieldSeq::get_BookmarkName. Obtiene o establece un nombre de marcador que se refiere a un elemento en otra parte del documento en lugar de la ubicación actual en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldseq/get_bookmarkname/
---
## FieldSeq::get_BookmarkName method


Obtiene o establece un nombre de marcador que se refiere a un elemento en otra parte del documento en lugar de la ubicación actual.

```cpp
System::String Aspose::Words::Fields::FieldSeq::get_BookmarkName()
```


## Ejemplos



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

* Class [FieldSeq](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
