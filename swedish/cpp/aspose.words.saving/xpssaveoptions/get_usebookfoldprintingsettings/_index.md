---
title: "Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings metod"
linktitle: "get_UseBookFoldPrintingSettings"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings metod. Hämtar eller anger ett booleskt värde som indikerar om dokumentet ska sparas med ett boktryckningslayout, om det anges via MultiplePages i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.saving/xpssaveoptions/get_usebookfoldprintingsettings/
---
## XpsSaveOptions::get_UseBookFoldPrintingSettings method


Hämtar eller anger ett booleskt värde som indikerar om dokumentet ska sparas med ett boktryckningslayout, om det anges via [MultiplePages](../../../aspose.words/pagesetup/get_multiplepages/).

```cpp
bool Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings() const
```

## Anmärkningar


Om detta alternativ anges, ignoreras [PageSet](../../fixedpagesaveoptions/get_pageset/) vid sparande. Detta beteende matchar MS Word. Om bokvikt‑utskriftsinställningar inte anges i sidinställningarna, har detta alternativ ingen effekt.

## Exempel



Visar hur man sparar ett dokument till XPS-formatet i form av en bokvikt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// Skapa ett "XpsSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .XPS.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>(Aspose::Words::SaveFormat::Xps);

// Ställ in egenskapen \"UseBookFoldPrintingSettings\" till \"true\" för att ordna innehållet
// i den exporterade XPS på ett sätt som hjälper oss att använda den för att skapa ett häfte.
// Ställ in egenskapen "UseBookFoldPrintingSettings" till "false" för att rendera XPS:n normalt.
xpsOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// Om vi renderar dokumentet som ett häfte måste vi ställa in \"MultiplePages\"
// egenskaperna för sidinställningsobjekten i alla sektioner till \"MultiplePagesType.BookFoldPrinting\".
if (renderTextAsBookFold)
{
    for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
    {
        s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
    }
}

// När vi skriver ut detta dokument kan vi göra det till ett häfte genom att stapla sidorna
// som kommer ut ur skrivaren och viker dem på mitten.
doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.BookFold.xps", xpsOptions);
```

## Se även

* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
