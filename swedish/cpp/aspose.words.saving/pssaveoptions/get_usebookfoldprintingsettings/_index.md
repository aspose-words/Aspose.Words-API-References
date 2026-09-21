---
title: "Aspose::Words::Saving::PsSaveOptions::get_UseBookFoldPrintingSettings‑metod"
linktitle: "get_UseBookFoldPrintingSettings"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PsSaveOptions::get_UseBookFoldPrintingSettings‑metod. Hämtar eller anger ett booleskt värde som indikerar om dokumentet ska sparas med en boktryckningslayout, om det anges via MultiplePages i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.saving/pssaveoptions/get_usebookfoldprintingsettings/
---
## PsSaveOptions::get_UseBookFoldPrintingSettings method


Hämtar eller anger ett booleskt värde som indikerar om dokumentet ska sparas med ett boktryckningslayout, om det anges via [MultiplePages](../../../aspose.words/pagesetup/get_multiplepages/).

```cpp
bool Aspose::Words::Saving::PsSaveOptions::get_UseBookFoldPrintingSettings() const
```

## Anmärkningar


Om detta alternativ anges, ignoreras [PageSet](../../fixedpagesaveoptions/get_pageset/) vid sparande. Detta beteende matchar MS Word. Om bokvikt‑utskriftsinställningar inte anges i sidinställningarna, har detta alternativ ingen effekt.

## Exempel



Visar hur man sparar ett dokument i Postscript‑formatet i form av en bokvikt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// Skapa ett \"PsSaveOptions\"‑objekt som vi kan skicka till dokumentets \"Save\"‑metod
// för att ändra hur den metoden konverterar dokumentet till PostScript.
// Ställ in egenskapen \"UseBookFoldPrintingSettings\" till \"true\" för att ordna innehållet
// i den utgående Postscript‑dokumentet på ett sätt som hjälper oss att göra en häfte av det.
// Ställ in egenskapen \"UseBookFoldPrintingSettings\" till \"false\" för att spara dokumentet normalt.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::PsSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Ps);
saveOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// Om vi renderar dokumentet som ett häfte måste vi ställa in \"MultiplePages\"
// egenskaperna för sidinställningsobjekten i alla sektioner till \"MultiplePagesType.BookFoldPrinting\".
for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
{
    s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
}

// När vi har skrivit ut detta dokument på båda sidor av sidorna kan vi vika alla sidor på mitten på en gång,
// och innehållet kommer att linjera på ett sätt som skapar ett häfte.
doc->Save(get_ArtifactsDir() + u"PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

## Se även

* Class [PsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
