---
title: "Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks‑metod"
linktitle: "get_ShowParagraphMarks"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks‑metod. Hämtar eller anger indikation på om stycketecken renderas. Standard är false i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.layout/layoutoptions/get_showparagraphmarks/
---
## LayoutOptions::get_ShowParagraphMarks method


Hämtar eller sätter indikation på om stycketecken renderas. Standard är **false**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks() const
```


## Exempel



Visar hur man visar stycketecken i ett renderat utdata-dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Lägg till några stycken och aktivera sedan stycketecken för att visa slutet på styckena
// med ett pilcrow‑symbol (¶) när vi renderar dokumentet.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```

## Se även

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
