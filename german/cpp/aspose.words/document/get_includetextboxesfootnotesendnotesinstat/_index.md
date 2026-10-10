---
title: "Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat Methode"
linktitle: "get_IncludeTextboxesFootnotesEndnotesInStat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat Methode. Gibt an, ob Textfelder, Fußnoten und Endnoten in die Wortzählstatistik einbezogen werden sollen in C++."
type: docs
weight: 33000
url: /de/cpp/aspose.words/document/get_includetextboxesfootnotesendnotesinstat/
---
## Document::get_IncludeTextboxesFootnotesEndnotesInStat method


Gibt an, ob Textfelder, Fußnoten und Endnoten in die Wortzählstatistik einbezogen werden sollen.

```cpp
bool Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat()
```


## Beispiele



Zeigt, wie Textfelder, Fußnoten und Endnoten in die Wortzählstatistik ein- oder ausgeschlossen werden können.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Lorem ipsum");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"sit amet");

// Standardmäßig ist die Option auf 'false' gesetzt.
doc->UpdateWordCount();
// Wortanzahl ohne Textfelder, Fußnoten und Endnoten.
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Words());

doc->set_IncludeTextboxesFootnotesEndnotesInStat(true);
doc->UpdateWordCount();
// Wortanzahl mit Textfeldern, Fußnoten und Endnoten.
ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Words());
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
