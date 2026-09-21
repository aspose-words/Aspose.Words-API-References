---
title: "Aspose::Words::PageSetup::get_LineStartingNumber metod"
linktitle: "get_LineStartingNumber"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_LineStartingNumber metod. Hämtar eller anger startlinjenummer i C++."
type: docs
weight: 27000
url: /sv/cpp/aspose.words/pagesetup/get_linestartingnumber/
---
## PageSetup::get_LineStartingNumber method


Hämtar eller anger startradnumret.

```cpp
int32_t Aspose::Words::PageSetup::get_LineStartingNumber()
```


## Exempel



Visar hur man aktiverar radnumrering för en sektion.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Vi kan använda sektionens PageSetup-objekt för att visa siffror till vänster om sektionens textrader.
// Detta är samma beteende som ett List-objekt,
// men det täcker hela sektionen och ändrar inte texten på något sätt.
// Vår sektion kommer att starta om numreringen på varje ny sida från 1 och visa siffran,
// om den är en multipel av 3, på 50pt till vänster om raden.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_LineStartingNumber(1);
pageSetup->set_LineNumberCountBy(3);
pageSetup->set_LineNumberRestartMode(Aspose::Words::LineNumberRestartMode::RestartPage);
pageSetup->set_LineNumberDistanceFromText(50.0);

for (int32_t i = 1; i <= 25; i++)
{
    builder->Writeln(System::String::Format(u"Line {0}.", i));
}

// Radräknaren kommer att hoppa över alla stycken med flaggan "SuppressLineNumbers" satt till "true".
// Detta stycke är på den 15:e raden, vilket är en multipel av 3, och skulle därför normalt visa ett radnummer.
// Sektionens radräknare kommer också att ignorera denna rad, behandla nästa rad som den 15:e,
// och fortsätta räknandet från den punkten och framåt.
doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(14)->get_ParagraphFormat()->set_SuppressLineNumbers(true);

doc->Save(get_ArtifactsDir() + u"PageSetup.LineNumbers.docx");
```

## Se även

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
