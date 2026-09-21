---
title: "Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat metod"
linktitle: "get_IncludeTextboxesFootnotesEndnotesInStat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat metod. Anger om textrutor, fotnoter och slutnoter ska inkluderas i statistik för ordantal i C++."
type: docs
weight: 33000
url: /sv/cpp/aspose.words/document/get_includetextboxesfootnotesendnotesinstat/
---
## Document::get_IncludeTextboxesFootnotesEndnotesInStat method


Anger om textrutor, fotnoter och slutnoter ska inkluderas i ordantalstatistik.

```cpp
bool Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat()
```


## Exempel



Visar hur man inkluderar eller exkluderar textrutor, fotnoter och slutnoter från ordantalstatistik.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Lorem ipsum");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"sit amet");

// Som standard är alternativet satt till 'false'.
doc->UpdateWordCount();
// Ordantal utan textrutor, fotnoter och slutnoter.
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Words());

doc->set_IncludeTextboxesFootnotesEndnotesInStat(true);
doc->UpdateWordCount();
// Ordantal med textrutor, fotnoter och slutnoter.
ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Words());
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
