---
title: "Aspose::Words::Document::ExtractPages metod"
linktitle: "ExtractPages"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::ExtractPages metod. Returnerar Document-objektet som representerar det angivna sidintervallet i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words/document/extractpages/
---
## Document::ExtractPages(int32_t, int32_t) method


Returnerar [Document](../)-objektet som representerar det angivna sidintervallet.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::ExtractPages(int32_t index, int32_t count)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | int32_t | Det nollbaserade indexet för den första sidan som ska extraheras. |
| count | int32_t | Antal sidor som ska extraheras. |

## Exempel



Visar hur man får det angivna sidintervallet från dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Layout entities.docx");

doc = doc->ExtractPages(0, 2);

doc->Save(get_ArtifactsDir() + u"Document.ExtractPages.docx");
```


Visa hur man återställer den ursprungliga sidnumreringen och sparar NUMPAGE-fältet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Page fields.docx");

// Standardbeteende:
// Den extraherade sidnumreringen är densamma som i originaldokumentet, som om vi hade valt "Print 2 pages" i MS Word.
// Startsidnumret kommer att sättas till 2 och fältet som indikerar antalet sidor kommer att tas bort
// och ersättas med ett konstant värde lika med antalet sidor.
System::SharedPtr<Aspose::Words::Document> extractedDoc1 = doc->ExtractPages(1, 1);
extractedDoc1->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Default.docx");

// Ändrat beteende:
// Den extraherade sidnumreringen återställs och en ny börjar,
// som om vi hade kopierat innehållet på den andra sidan och klistrat in det i ett nytt dokument.
// Startsidnumret kommer att sättas till 1 och fältet som indikerar antalet sidor kommer att lämnas oförändrat
// och kommer att visa det aktuella antalet sidor.
auto extractOptions = System::MakeObject<Aspose::Words::PageExtractOptions>();
extractOptions->set_UpdatePageStartingNumber(false);
extractOptions->set_UnlinkPagesNumberFields(false);
System::SharedPtr<Aspose::Words::Document> extractedDoc2 = doc->ExtractPages(1, 1, extractOptions);
extractedDoc2->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Options.docx");
```

## Se även

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::ExtractPages(int32_t, int32_t, const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\&) method


Returnerar [Document](../)-objektet som representerar det angivna sidintervallet och de angivna extraheringsalternativen för sidan.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::ExtractPages(int32_t index, int32_t count, const System::SharedPtr<Aspose::Words::PageExtractOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | int32_t | Det nollbaserade indexet för den första sidan som ska extraheras. |
| count | int32_t | Antal sidor som ska extraheras. |
| options | const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\& | Tillhandahåller alternativ för att hantera sidextraheringsprocessen. |

## Se även

* Class [Document](../)
* Class [PageExtractOptions](../../pageextractoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
