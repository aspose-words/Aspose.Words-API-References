---
title: "Aspose::Words::PageSetup::get_SheetsPerBooklet metod"
linktitle: "get_SheetsPerBooklet"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_SheetsPerBooklet metod. Returnerar eller anger antalet sidor som ska inkluderas i varje häfte i C++."
type: docs
weight: 42000
url: /sv/cpp/aspose.words/pagesetup/get_sheetsperbooklet/
---
## PageSetup::get_SheetsPerBooklet method


Returnerar eller anger antalet sidor som ska inkluderas i varje häfte.

```cpp
int32_t Aspose::Words::PageSetup::get_SheetsPerBooklet() const
```


## Exempel



Visar hur man konfigurerar ett dokument som kan skrivas ut som en bokvikt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Infoga text som sträcker sig över 16 sidor.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"My Booklet:");

for (int32_t i = 0; i < 15; i++)
{
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
    builder->Write(System::String::Format(u"Booklet face #{0}", i));
}

// Konfigurera den första sektionens egenskap "PageSetup" för att skriva ut dokumentet i form av en bokvikt.
// När vi skriver ut detta dokument på båda sidor kan vi ta sidorna för att stapla dem
// och vika dem alla ner i mitten på en gång. Dokumentets innehåll kommer att radas upp till en bokvikt.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);

// Vi kan endast ange antalet ark i multiplar av 4.
pageSetup->set_SheetsPerBooklet(4);

doc->Save(get_ArtifactsDir() + u"PageSetup.Booklet.docx");
```

## Se även

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
