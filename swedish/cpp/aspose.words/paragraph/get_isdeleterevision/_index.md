---
title: "Aspose::Words::Paragraph::get_IsDeleteRevision metod"
linktitle: "get_IsDeleteRevision"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Paragraph::get_IsDeleteRevision metod. Returnerar true om detta objekt raderades i Microsoft Word medan spårning av ändringar var aktiverad i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words/paragraph/get_isdeleterevision/
---
## Paragraph::get_IsDeleteRevision method


Returnerar true om detta objekt raderades i Microsoft Word medan spårning av ändringar var aktiverad.

```cpp
bool Aspose::Words::Paragraph::get_IsDeleteRevision()
```


## Exempel



Visar hur man arbetar med revisionsstycken.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Body> body = doc->get_FirstSection()->get_Body();
System::SharedPtr<Aspose::Words::Paragraph> para = body->get_FirstParagraph();

para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Paragraph 1. "));
body->AppendParagraph(u"Paragraph 2. ");
body->AppendParagraph(u"Paragraph 3. ");

// Ovanstående stycken är inte revisioner.
// Stycken som vi lägger till efter att ha startat revisionsspårning kommer att registreras som "Insert"-revisioner.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());

para = body->AppendParagraph(u"Paragraph 4. ");

ASSERT_TRUE(para->get_IsInsertRevision());

// Stycken som vi tar bort efter att ha startat revisionsspårning kommer att registreras som "Delete"-revisioner.
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = body->get_Paragraphs();

ASSERT_EQ(4, paragraphs->get_Count());

para = paragraphs->idx_get(2);
para->Remove();

// Sådana stycken kommer att kvarstå tills vi antingen accepterar eller förkastar raderingsrevisionen.
// Att acceptera revisionen kommer att ta bort stycket för gott,
// och att förkasta revisionen kommer att lämna det i dokumentet som om vi aldrig hade raderat det.
ASSERT_EQ(4, paragraphs->get_Count());
ASSERT_TRUE(para->get_IsDeleteRevision());

// Acceptera revisionen och verifiera sedan att stycket är borta.
doc->AcceptAllRevisions();

ASSERT_EQ(3, paragraphs->get_Count());
ASSERT_EQ(0, para->get_Count());
ASSERT_EQ(System::String(u"Paragraph 1. \r") + u"Paragraph 2. \r" + u"Paragraph 4.", doc->GetText().Trim());
```

## Se även

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
