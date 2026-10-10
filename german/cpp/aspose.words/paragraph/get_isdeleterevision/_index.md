---
title: "Aspose::Words::Paragraph::get_IsDeleteRevision Methode"
linktitle: "get_IsDeleteRevision"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Paragraph::get_IsDeleteRevision Methode. Gibt wahr zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung in C++ aktiviert war."
type: docs
weight: 7000
url: /de/cpp/aspose.words/paragraph/get_isdeleterevision/
---
## Paragraph::get_IsDeleteRevision method


Gibt true zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war.

```cpp
bool Aspose::Words::Paragraph::get_IsDeleteRevision()
```


## Beispiele



Zeigt, wie man mit Revisionsabsätzen arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Body> body = doc->get_FirstSection()->get_Body();
System::SharedPtr<Aspose::Words::Paragraph> para = body->get_FirstParagraph();

para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Paragraph 1. "));
body->AppendParagraph(u"Paragraph 2. ");
body->AppendParagraph(u"Paragraph 3. ");

// Die obigen Absätze sind keine Revisionen.
// Absätze, die wir nach dem Start der Nachverfolgung von Änderungen hinzufügen, werden als "Insert"-Revisionen registriert.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());

para = body->AppendParagraph(u"Paragraph 4. ");

ASSERT_TRUE(para->get_IsInsertRevision());

// Absätze, die wir nach dem Start der Nachverfolgung von Änderungen entfernen, werden als "Delete"-Revisionen registriert.
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = body->get_Paragraphs();

ASSERT_EQ(4, paragraphs->get_Count());

para = paragraphs->idx_get(2);
para->Remove();

// Solche Absätze bleiben erhalten, bis wir die Löschrevision entweder akzeptieren oder ablehnen.
// Das Akzeptieren der Revision entfernt den Absatz endgültig,
// und das Ablehnen der Revision lässt ihn im Dokument zurück, als hätten wir ihn nie gelöscht.
ASSERT_EQ(4, paragraphs->get_Count());
ASSERT_TRUE(para->get_IsDeleteRevision());

// Akzeptieren Sie die Revision und überprüfen Sie anschließend, dass der Absatz verschwunden ist.
doc->AcceptAllRevisions();

ASSERT_EQ(3, paragraphs->get_Count());
ASSERT_EQ(0, para->get_Count());
ASSERT_EQ(System::String(u"Paragraph 1. \r") + u"Paragraph 2. \r" + u"Paragraph 4.", doc->GetText().Trim());
```

## Siehe auch

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
