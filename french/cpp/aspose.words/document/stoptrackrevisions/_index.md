---
title: "Aspose::Words::Document::StopTrackRevisions méthode"
linktitle: "StopTrackRevisions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::StopTrackRevisions méthode. Arrête le marquage automatique des modifications du document en tant que révisions en C++."
type: docs
weight: 93000
url: /fr/cpp/aspose.words/document/stoptrackrevisions/
---
## Document::StopTrackRevisions method


Arrête le marquage automatique des modifications du document en tant que révisions.

```cpp
void Aspose::Words::Document::StopTrackRevisions()
```


## Exemples



Montre comment suivre les révisions lors de l'édition d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// L'édition d'un document n'est généralement pas comptée comme une révision tant que nous n'avons pas commencé à les suivre.
builder->Write(u"Hello world! ");

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_IsInsertRevision());

doc->StartTrackRevisions(u"John Doe");

builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(1)->get_IsInsertRevision());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
ASSERT_TRUE((System::DateTime::get_Now() - doc->get_Revisions()->idx_get(0)->get_DateTime()).get_Milliseconds() <= 10);

// Arrêtez le suivi des révisions pour ne pas compter les futures modifications comme des révisions.
doc->StopTrackRevisions();
builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(2)->get_IsInsertRevision());

// Créer des révisions leur attribue une date et une heure de l'opération.
// Nous pouvons désactiver cela en passant DateTime.MinValue lorsque nous commençons à suivre les révisions.
doc->StartTrackRevisions(u"John Doe", System::DateTime::MinValue);
builder->Write(u"Hello again! ");

ASSERT_EQ(2, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(1)->get_Author());
ASSERT_EQ(System::DateTime::MinValue, doc->get_Revisions()->idx_get(1)->get_DateTime());

// Nous pouvons accepter/rejeter ces révisions de manière programmatique
// en appelant des méthodes telles que Document.AcceptAllRevisions, ou la méthode Accept de chaque révision.
// Dans Microsoft Word, nous pouvons les traiter manuellement via "Review" -> "Changes".
doc->Save(get_ArtifactsDir() + u"Revision.StartTrackRevisions.docx");
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
