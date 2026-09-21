---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Lines metod"
linktitle: "get_Lines"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Lines metod. Representerar en uppskattning av antalet rader i dokumentet i C++."
type: docs
weight: 18000
url: /sv/cpp/aspose.words.properties/builtindocumentproperties/get_lines/
---
## BuiltInDocumentProperties::get_Lines method


Representerar en uppskattning av antalet rader i dokumentet.

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_Lines()
```

## Anmärkningar


Aspose.Words uppdaterar den här egenskapen när du anropar [UpdateWordCount()](../../../aspose.words/document/updatewordcount/).

## Exempel



Visar hur man uppdaterar alla listetiketter i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"Ut enim ad minim veniam, ") + u"quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words spårar inte dokumentmetrik som dessa i realtid.
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Paragraphs());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

// För att få korrekta värden för tre av dessa egenskaper måste vi uppdatera dem manuellt.
doc->UpdateWordCount();

ASSERT_EQ(196, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(36, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Paragraphs());

// För radantalet måste vi anropa en specifik överlagring av uppdateringsmetoden.
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

doc->UpdateWordCount(true);

ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Lines());
```

## Se även

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
