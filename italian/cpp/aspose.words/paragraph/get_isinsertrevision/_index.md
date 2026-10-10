---
title: "Aspose::Words::Paragraph::get_IsInsertRevision method"
linktitle: "get_IsInsertRevision"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Paragraph::get_IsInsertRevision method. Restituisce vero se questo oggetto è stato inserito in Microsoft Word mentre il tracciamento delle modifiche era abilitato in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words/paragraph/get_isinsertrevision/
---
## Paragraph::get_IsInsertRevision method


Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre il tracciamento delle modifiche era abilitato.

```cpp
bool Aspose::Words::Paragraph::get_IsInsertRevision()
```


## Esempi



Mostra come lavorare con i paragrafi di revisione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Body> body = doc->get_FirstSection()->get_Body();
System::SharedPtr<Aspose::Words::Paragraph> para = body->get_FirstParagraph();

para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Paragraph 1. "));
body->AppendParagraph(u"Paragraph 2. ");
body->AppendParagraph(u"Paragraph 3. ");

// I paragrafi sopra non sono revisioni.
// I paragrafi che aggiungiamo dopo aver avviato il tracciamento delle revisioni verranno registrati come revisioni "Insert".
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());

para = body->AppendParagraph(u"Paragraph 4. ");

ASSERT_TRUE(para->get_IsInsertRevision());

// I paragrafi che rimuoviamo dopo aver avviato il tracciamento delle revisioni verranno registrati come revisioni "Delete".
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = body->get_Paragraphs();

ASSERT_EQ(4, paragraphs->get_Count());

para = paragraphs->idx_get(2);
para->Remove();

// Tali paragrafi rimarranno finché non accetteremo o rifiuteremo la revisione di cancellazione.
// Accettare la revisione rimuoverà il paragrafo definitivamente,
// e rifiutare la revisione lo lascerà nel documento come se non lo avessimo mai cancellato.
ASSERT_EQ(4, paragraphs->get_Count());
ASSERT_TRUE(para->get_IsDeleteRevision());

// Accetta la revisione, quindi verifica che il paragrafo sia scomparso.
doc->AcceptAllRevisions();

ASSERT_EQ(3, paragraphs->get_Count());
ASSERT_EQ(0, para->get_Count());
ASSERT_EQ(System::String(u"Paragraph 1. \r") + u"Paragraph 2. \r" + u"Paragraph 4.", doc->GetText().Trim());
```

## Vedi anche

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
