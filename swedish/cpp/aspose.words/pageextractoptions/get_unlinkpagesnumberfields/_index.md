---
title: "Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields metod"
linktitle: "get_UnlinkPagesNumberFields"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields metod. Anger om NUMPAGES-fält i det resulterande dokumentet ska ersättas med deras faktiska resulterande värden. Standardvärdet är true i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/pageextractoptions/get_unlinkpagesnumberfields/
---
## PageExtractOptions::get_UnlinkPagesNumberFields method


Anger om NUMPAGES-fält i det resulterande dokumentet ska ersättas med deras faktiska värden. Standardvärdet är **true**.

```cpp
bool Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields() const
```


## Exempel



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

* Class [PageExtractOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
