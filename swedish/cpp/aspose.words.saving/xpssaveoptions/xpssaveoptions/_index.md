---
title: "Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions konstruktor"
linktitle: "XpsSaveOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions konstruktor. Initierar en ny instans av denna klass som kan användas för att spara ett dokument i Xps-formatet i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions::XpsSaveOptions() constructor


Initierar en ny instans av den här klassen som kan användas för att spara ett dokument i [Xps](../../../aspose.words/saveformat/) formatet.

```cpp
Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions()
```


## Exempel



Visar hur man begränsar rubriknivån som kommer att visas i konturen av ett sparat XPS-dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga rubriker som kan fungera som innehållsförteckningsposter på nivå 1, 2 och sedan 3.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);

builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);

builder->Writeln(u"Heading 1.2.1");
builder->Writeln(u"Heading 1.2.2");

// Skapa ett "XpsSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .XPS.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Xps, saveOptions->get_SaveFormat());

// Det resulterande XPS-dokumentet kommer att innehålla en kontur, en innehållsförteckning som listar rubriker i dokumentets huvuddel.
// Att klicka på en post i denna kontur tar oss till platsen för dess respektive rubrik.
// Ställ in egenskapen "HeadingsOutlineLevels" till "2" för att utesluta alla rubriker vars nivåer är över 2 från konturen.
// De två sista rubrikerna vi har infogat ovan kommer inte att visas.
saveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(2);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

## Se även

* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## XpsSaveOptions::XpsSaveOptions(Aspose::Words::SaveFormat) constructor


Initierar en ny instans av den här klassen som kan användas för att spara ett dokument i [Xps](../../../aspose.words/saveformat/) eller [OpenXps](../../../aspose.words/saveformat/) formatet.

```cpp
Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
