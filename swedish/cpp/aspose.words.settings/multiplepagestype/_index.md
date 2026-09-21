---
title: "Aspose::Words::Settings::MultiplePagesType enum"
linktitle: "MultiplePagesType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::MultiplePagesType enum. Anger hur dokumentet skrivs ut i C++."
type: docs
weight: 18000
url: /sv/cpp/aspose.words.settings/multiplepagestype/
---
## MultiplePagesType enum


Anger hur dokumentet skrivs ut.

```cpp
enum class MultiplePagesType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Normal | 0 | Normal utskrift, inga flera sidor specificerade. |
| MirrorMargins | 1 | Byter plats på vänster och höger marginal på motsatta sidor. |
| TwoPagesPerSheet | 2 | Skriver ut två sidor per ark. |
| BookFoldPrinting | 3 | Anger om dokumentet ska skrivas ut som en bokvikt. |
| BookFoldPrintingReverse | 4 | Anger om dokumentet ska skrivas ut som en omvänd bokvikt. |
| Default | n/a | Standardvärdet är [Normal](./) |


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

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
