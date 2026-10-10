---
title: "Aspose::Words::Document::StopTrackRevisions-Methode"
linktitle: "StopTrackRevisions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::StopTrackRevisions-Methode. Stoppt die automatische Kennzeichnung von Dokumentänderungen als Revisionen in C++."
type: docs
weight: 93000
url: /de/cpp/aspose.words/document/stoptrackrevisions/
---
## Document::StopTrackRevisions method


Stoppt die automatische Markierung von Dokumentänderungen als Revisionen.

```cpp
void Aspose::Words::Document::StopTrackRevisions()
```


## Beispiele



Zeigt, wie man Revisionen beim Bearbeiten eines Dokuments verfolgt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Das Bearbeiten eines Dokuments wird normalerweise nicht als Revision gezählt, bis wir mit der Verfolgung beginnen.
builder->Write(u"Hello world! ");

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_IsInsertRevision());

doc->StartTrackRevisions(u"John Doe");

builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(1)->get_IsInsertRevision());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
ASSERT_TRUE((System::DateTime::get_Now() - doc->get_Revisions()->idx_get(0)->get_DateTime()).get_Milliseconds() <= 10);

// Stoppen Sie die Verfolgung von Revisionen, damit zukünftige Änderungen nicht als Revisionen gezählt werden.
doc->StopTrackRevisions();
builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(2)->get_IsInsertRevision());

// Das Erstellen von Revisionen gibt ihnen ein Datum und eine Uhrzeit der Operation.
// Wir können dies deaktivieren, indem wir DateTime.MinValue übergeben, wenn wir die Verfolgung von Revisionen starten.
doc->StartTrackRevisions(u"John Doe", System::DateTime::MinValue);
builder->Write(u"Hello again! ");

ASSERT_EQ(2, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(1)->get_Author());
ASSERT_EQ(System::DateTime::MinValue, doc->get_Revisions()->idx_get(1)->get_DateTime());

// Wir können diese Revisionen programmgesteuert akzeptieren/ablehnen
// indem wir Methoden wie Document.AcceptAllRevisions oder die Accept-Methode jeder einzelnen Revision aufrufen.
// In Microsoft Word können wir sie manuell über \"Review\" -> \"Changes\" verarbeiten.
doc->Save(get_ArtifactsDir() + u"Revision.StartTrackRevisions.docx");
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
