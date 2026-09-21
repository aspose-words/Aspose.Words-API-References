---
title: "Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries‑metod"
linktitle: "get_DoNotDisplayPageBoundaries"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries‑metod. Stänger av visning av utrymmet mellan textens topp och sidans övre kant i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.settings/viewoptions/get_donotdisplaypageboundaries/
---
## ViewOptions::get_DoNotDisplayPageBoundaries method


Stänger av visning av utrymmet mellan textens överkant och sidans övre kant.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries() const
```


## Exempel



Visar hur man döljer vertikalt blanksteg samt sidhuvuden/sidfötter i visningsalternativ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga innehåll som sträcker sig över 3 sidor.
builder->Writeln(u"Paragraph 1, Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Paragraph 2, Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Paragraph 3, Page 3.");

// Infoga ett sidhuvud och en sidfot.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"This is the header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"This is the footer.");

// Detta dokument innehåller en liten mängd innehåll som tar upp några hela sidor.
// Ställ in flaggan "DoNotDisplayPageBoundaries" till "true" för att äldre versioner av Microsoft Word ska utelämna sidhuvuden,
// sidfötter och mycket av det vertikala blanksteget när dokumentet visas.
// Ställ in flaggan "DoNotDisplayPageBoundaries" till "false" för att äldre versioner av Microsoft Word
// ska visa vårt dokument normalt.
doc->get_ViewOptions()->set_DoNotDisplayPageBoundaries(doNotDisplayPageBoundaries);

doc->Save(get_ArtifactsDir() + u"ViewOptions.DisplayPageBoundaries.doc");
```

## Se även

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
