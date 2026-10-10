---
title: "Aspose::Words::PageSetup::get_Bidi metod"
linktitle: "get_Bidi"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_Bidi metod. Anger att detta avsnitt innehåller bidirektionell (komplexa skript) text i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/pagesetup/get_bidi/
---
## PageSetup::get_Bidi method


Anger att detta avsnitt innehåller tvåvägs (komplexa skript) text.

```cpp
bool Aspose::Words::PageSetup::get_Bidi()
```

## Anmärkningar


När **true**, är kolumnerna i detta avsnitt placerade från höger till vänster.

## Exempel



Visar hur man ställer in ordningen på textkolumner i ett avsnitt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_TextColumns()->SetCount(3);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Write(u"Column 2.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Write(u"Column 3.");

// Ställ in egenskapen "Bidi" till "true" för att ordna kolumnerna med början från sidans högra sida.
// Kolumnordningen kommer att matcha riktningen för höger-till-vänster-texten.
// Ställ in egenskapen "Bidi" till "false" för att ordna kolumnerna med början från sidans vänstra sida.
// Kolumnordningen kommer att matcha riktningen för vänster-till-höger-texten.
pageSetup->set_Bidi(reverseColumns);

doc->Save(get_ArtifactsDir() + u"PageSetup.Bidi.docx");
```

## Se även

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
