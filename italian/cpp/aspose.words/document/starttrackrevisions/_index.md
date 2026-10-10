---
title: "Metodo Aspose::Words::Document::StartTrackRevisions"
linktitle: "StartTrackRevisions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Document::StartTrackRevisions. Inizia a contrassegnare automaticamente tutte le modifiche successive apportate al documento programmaticamente come modifiche di revisione in C++."
type: docs
weight: 92000
url: /it/cpp/aspose.words/document/starttrackrevisions/
---
## Document::StartTrackRevisions(const System::String\&) method


Inizia a contrassegnare automaticamente tutte le modifiche successive che apporti al documento programmaticamente come modifiche di revisione.

```cpp
void Aspose::Words::Document::StartTrackRevisions(const System::String &author)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| autore | const System::String\& | Iniziali dell'autore da utilizzare per le revisioni. |
## Note


Se chiami questo metodo e poi apporti alcune modifiche al documento programmaticamente, salvi il documento e successivamente lo apri in MS Word, vedrai queste modifiche come revisioni.

Attualmente Aspose.Words supporta il tracciamento solo delle inserzioni e cancellazioni di nodi. Le modifiche di formattazione non vengono registrate come revisioni.

Il tracciamento automatico delle modifiche è supportato sia durante la modifica di questo documento tramite manipolazioni dei nodi sia quando si utilizza [DocumentBuilder](../../documentbuilder/)

Questo metodo non modifica l'opzione [TrackRevisions](../get_trackrevisions/) e non utilizza il suo valore ai fini del tracciamento delle revisioni.

## Esempi



Mostra come tracciare le revisioni durante la modifica di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Modificare un documento di solito non conta come revisione finché non iniziamo a tracciarle.
builder->Write(u"Hello world! ");

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_IsInsertRevision());

doc->StartTrackRevisions(u"John Doe");

builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(1)->get_IsInsertRevision());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
ASSERT_TRUE((System::DateTime::get_Now() - doc->get_Revisions()->idx_get(0)->get_DateTime()).get_Milliseconds() <= 10);

// Interrompi il tracciamento delle revisioni per non contare le modifiche future come revisioni.
doc->StopTrackRevisions();
builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(2)->get_IsInsertRevision());

// Creare revisioni assegna loro una data e un'ora dell'operazione.
// Possiamo disabilitare questo passando DateTime.MinValue quando iniziamo a tenere traccia delle revisioni.
doc->StartTrackRevisions(u"John Doe", System::DateTime::MinValue);
builder->Write(u"Hello again! ");

ASSERT_EQ(2, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(1)->get_Author());
ASSERT_EQ(System::DateTime::MinValue, doc->get_Revisions()->idx_get(1)->get_DateTime());

// Possiamo accettare/rifiutare queste revisioni programmaticamente
// chiamando metodi come Document.AcceptAllRevisions, o il metodo Accept di ogni revisione.
// In Microsoft Word, possiamo elaborarli manualmente tramite "Review" -> "Changes".
doc->Save(get_ArtifactsDir() + u"Revision.StartTrackRevisions.docx");
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::StartTrackRevisions(const System::String\&, System::DateTime) method


Inizia a contrassegnare automaticamente tutte le modifiche successive che apporti al documento programmaticamente come modifiche di revisione.

```cpp
void Aspose::Words::Document::StartTrackRevisions(const System::String &author, System::DateTime dateTime)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| autore | const System::String\& | Iniziali dell'autore da utilizzare per le revisioni. |
| dateTime | System::DateTime | La data e l'ora da utilizzare per le revisioni. |
## Note


Se chiami questo metodo e poi apporti alcune modifiche al documento programmaticamente, salvi il documento e successivamente lo apri in MS Word, vedrai queste modifiche come revisioni.

Attualmente Aspose.Words supporta il tracciamento solo delle inserzioni e cancellazioni di nodi. Le modifiche di formattazione non vengono registrate come revisioni.

Il tracciamento automatico delle modifiche è supportato sia durante la modifica di questo documento tramite manipolazioni dei nodi sia quando si utilizza [DocumentBuilder](../../documentbuilder/)

Questo metodo non modifica l'opzione [TrackRevisions](../get_trackrevisions/) e non utilizza il suo valore ai fini del tracciamento delle revisioni.

## Esempi



Mostra come tracciare le revisioni durante la modifica di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Modificare un documento di solito non conta come revisione finché non iniziamo a tracciarle.
builder->Write(u"Hello world! ");

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_IsInsertRevision());

doc->StartTrackRevisions(u"John Doe");

builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(1)->get_IsInsertRevision());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
ASSERT_TRUE((System::DateTime::get_Now() - doc->get_Revisions()->idx_get(0)->get_DateTime()).get_Milliseconds() <= 10);

// Interrompi il tracciamento delle revisioni per non contare le modifiche future come revisioni.
doc->StopTrackRevisions();
builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(2)->get_IsInsertRevision());

// Creare revisioni assegna loro una data e un'ora dell'operazione.
// Possiamo disabilitare questo passando DateTime.MinValue quando iniziamo a tenere traccia delle revisioni.
doc->StartTrackRevisions(u"John Doe", System::DateTime::MinValue);
builder->Write(u"Hello again! ");

ASSERT_EQ(2, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(1)->get_Author());
ASSERT_EQ(System::DateTime::MinValue, doc->get_Revisions()->idx_get(1)->get_DateTime());

// Possiamo accettare/rifiutare queste revisioni programmaticamente
// chiamando metodi come Document.AcceptAllRevisions, o il metodo Accept di ogni revisione.
// In Microsoft Word, possiamo elaborarli manualmente tramite "Review" -> "Changes".
doc->Save(get_ArtifactsDir() + u"Revision.StartTrackRevisions.docx");
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
