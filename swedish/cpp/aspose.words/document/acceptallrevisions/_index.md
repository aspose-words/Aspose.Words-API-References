---
title: "Aspose::Words::Document::AcceptAllRevisions metod"
linktitle: "AcceptAllRevisions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::AcceptAllRevisions metod. Accepterar alla spårade ändringar i dokumentet i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/document/acceptallrevisions/
---
## Document::AcceptAllRevisions method


Accepterar alla spårade ändringar i dokumentet.

```cpp
void Aspose::Words::Document::AcceptAllRevisions()
```


## Exempel



Visar hur man accepterar alla spårade ändringar i dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Redigera dokumentet medan du spårar ändringar för att skapa några revisioner.
doc->StartTrackRevisions(u"John Doe");
builder->Write(u"Hello world! ");
builder->Write(u"Hello again! ");
builder->Write(u"This is another revision.");
doc->StopTrackRevisions();

ASSERT_EQ(3, doc->get_Revisions()->get_Count());

// Vi kan iterera genom varje revision och acceptera/avvisa den som en del av vårt dokument.
// Om vi vet att vi vill acceptera varje revision kan vi göra det på ett enklare sätt genom att anropa den här metoden.
doc->AcceptAllRevisions();

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"Hello world! Hello again! This is another revision.", doc->GetText().Trim());
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
