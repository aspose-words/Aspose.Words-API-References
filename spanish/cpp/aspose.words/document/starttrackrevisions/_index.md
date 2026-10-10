---
title: "Aspose::Words::Document::StartTrackRevisions método"
linktitle: "StartTrackRevisions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::StartTrackRevisions método. Inicia marcando automáticamente todos los cambios posteriores que realice en el documento de forma programática como cambios de revisión en C++."
type: docs
weight: 92000
url: /es/cpp/aspose.words/document/starttrackrevisions/
---
## Document::StartTrackRevisions(const System::String\&) method


Comienza a marcar automáticamente todos los cambios posteriores que realices en el documento de forma programática como cambios de revisión.

```cpp
void Aspose::Words::Document::StartTrackRevisions(const System::String &author)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| autor | const System::String\& | Iniciales del autor a usar para revisiones. |
## Observaciones


Si llama a este método y luego realiza algunos cambios en el documento de forma programática, guarda el documento y más tarde lo abre en MS Word, verá estos cambios como revisiones.

Actualmente Aspose.Words solo admite el seguimiento de inserciones y eliminaciones de nodos. Los cambios de formato no se registran como revisiones.

El seguimiento automático de cambios es compatible tanto al modificar este documento mediante manipulaciones de nodos como al usar [DocumentBuilder](../../documentbuilder/)

Este método no modifica la opción [TrackRevisions](../get_trackrevisions/) y no utiliza su valor para el seguimiento de revisiones.

## Ejemplos



Muestra cómo rastrear revisiones mientras se edita un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Editar un documento normalmente no cuenta como una revisión hasta que comenzamos a rastrearlas.
builder->Write(u"Hello world! ");

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_IsInsertRevision());

doc->StartTrackRevisions(u"John Doe");

builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(1)->get_IsInsertRevision());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
ASSERT_TRUE((System::DateTime::get_Now() - doc->get_Revisions()->idx_get(0)->get_DateTime()).get_Milliseconds() <= 10);

// Detenga el seguimiento de revisiones para que no se cuenten ediciones futuras como revisiones.
doc->StopTrackRevisions();
builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(2)->get_IsInsertRevision());

// Crear revisiones les asigna una fecha y hora de la operación.
// Podemos desactivar esto pasando DateTime.MinValue cuando comenzamos a rastrear revisiones.
doc->StartTrackRevisions(u"John Doe", System::DateTime::MinValue);
builder->Write(u"Hello again! ");

ASSERT_EQ(2, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(1)->get_Author());
ASSERT_EQ(System::DateTime::MinValue, doc->get_Revisions()->idx_get(1)->get_DateTime());

// Podemos aceptar/rechazar estas revisiones programáticamente
// llamando a métodos como Document.AcceptAllRevisions, o al método Accept de cada revisión.
// En Microsoft Word, podemos procesarlas manualmente a través de "Revisar" -> "Cambios".
doc->Save(get_ArtifactsDir() + u"Revision.StartTrackRevisions.docx");
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::StartTrackRevisions(const System::String\&, System::DateTime) method


Comienza a marcar automáticamente todos los cambios posteriores que realices en el documento de forma programática como cambios de revisión.

```cpp
void Aspose::Words::Document::StartTrackRevisions(const System::String &author, System::DateTime dateTime)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| autor | const System::String\& | Iniciales del autor a usar para revisiones. |
| dateTime | System::DateTime | La fecha y hora a usar para las revisiones. |
## Observaciones


Si llama a este método y luego realiza algunos cambios en el documento de forma programática, guarda el documento y más tarde lo abre en MS Word, verá estos cambios como revisiones.

Actualmente Aspose.Words solo admite el seguimiento de inserciones y eliminaciones de nodos. Los cambios de formato no se registran como revisiones.

El seguimiento automático de cambios es compatible tanto al modificar este documento mediante manipulaciones de nodos como al usar [DocumentBuilder](../../documentbuilder/)

Este método no modifica la opción [TrackRevisions](../get_trackrevisions/) y no utiliza su valor para el seguimiento de revisiones.

## Ejemplos



Muestra cómo rastrear revisiones mientras se edita un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Editar un documento normalmente no cuenta como una revisión hasta que comenzamos a rastrearlas.
builder->Write(u"Hello world! ");

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_IsInsertRevision());

doc->StartTrackRevisions(u"John Doe");

builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(1)->get_IsInsertRevision());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
ASSERT_TRUE((System::DateTime::get_Now() - doc->get_Revisions()->idx_get(0)->get_DateTime()).get_Milliseconds() <= 10);

// Detenga el seguimiento de revisiones para que no se cuenten ediciones futuras como revisiones.
doc->StopTrackRevisions();
builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(2)->get_IsInsertRevision());

// Crear revisiones les asigna una fecha y hora de la operación.
// Podemos desactivar esto pasando DateTime.MinValue cuando comenzamos a rastrear revisiones.
doc->StartTrackRevisions(u"John Doe", System::DateTime::MinValue);
builder->Write(u"Hello again! ");

ASSERT_EQ(2, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(1)->get_Author());
ASSERT_EQ(System::DateTime::MinValue, doc->get_Revisions()->idx_get(1)->get_DateTime());

// Podemos aceptar/rechazar estas revisiones programáticamente
// llamando a métodos como Document.AcceptAllRevisions, o al método Accept de cada revisión.
// En Microsoft Word, podemos procesarlas manualmente a través de "Revisar" -> "Cambios".
doc->Save(get_ArtifactsDir() + u"Revision.StartTrackRevisions.docx");
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
