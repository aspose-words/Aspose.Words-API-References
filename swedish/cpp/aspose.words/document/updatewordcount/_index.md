---
title: "Aspose::Words::Document::UpdateWordCount metod"
linktitle: "UpdateWordCount"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::UpdateWordCount metod. Uppdaterar ordantalsegenskaperna i dokumentet i C++."
type: docs
weight: 101000
url: /sv/cpp/aspose.words/document/updatewordcount/
---
## Document::UpdateWordCount() method


Uppdaterar ordantalsegenskaperna för dokumentet.

```cpp
void Aspose::Words::Document::UpdateWordCount()
```

## Anmärkningar


[UpdateWordCount](./) recalculates and updates Characters, [Words](../../) and Paragraphs properties in the [BuiltInDocumentProperties](../get_builtindocumentproperties/) collection of the [Document](../).

Observera att [UpdateWordCount](./) inte uppdaterar egenskaperna för antal rader och sidor. Använd [UpdateWordCount](./) overload och skicka **true** som parameter för att göra det.

När du använder en utvärderingsversion kommer utvärderingsvattenstämpeln också att inkluderas i ordantalet.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::UpdateWordCount(bool) method


Uppdaterar ordantalsegenskaperna för dokumentet, uppdaterar valfritt egenskapen [Lines](../../../aspose.words.properties/builtindocumentproperties/get_lines/).

```cpp
void Aspose::Words::Document::UpdateWordCount(bool updateLinesCount)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| updateLinesCount | bool | **true** om antalet rader i dokumentet ska beräknas. |

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
