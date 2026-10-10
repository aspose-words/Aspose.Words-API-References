---
title: "Aspose::Words::Lists::ListLevel::get_IsLegal method"
linktitle: "get_IsLegal"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Lists::ListLevel::get_IsLegal method. Sant om nivån omvandlar alla ärvda nummer till arabiska, falskt om den behåller deras nummerstil i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.lists/listlevel/get_islegal/
---
## ListLevel::get_IsLegal method


Sant om nivån omvandlar alla ärvda nummer till arabiska, falskt om den behåller deras talstil.

```cpp
bool Aspose::Words::Lists::ListLevel::get_IsLegal() const
```


## Exempel



Visar avancerade sätt att anpassa listetiketter.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
// Vi kan skapa nästlade listor genom att öka indragnivån.
// Vi kan börja och avsluta en lista genom att använda en dokumentbyggares egenskap "ListFormat".
// Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

// Etiketter på nivå 1 kommer att formateras enligt styckeformatet "Heading 1" och får ett prefix.
// Dessa kommer att se ut som "Appendix A", "Appendix B"...
list->get_ListLevels()->idx_get(0)->set_NumberFormat(u"Appendix \x0000");
list->get_ListLevels()->idx_get(0)->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseLetter);
list->get_ListLevels()->idx_get(0)->set_LinkedStyle(doc->get_Styles()->idx_get(u"Heading 1"));

// Etiketter på nivå 2 visar de aktuella siffrorna för den första och den andra listnivån och har inledande nollor.
// Om den första listnivån är 1, kommer etiketter från dessa att se ut som "Section (1.01)", "Section (1.02)"...
list->get_ListLevels()->idx_get(1)->set_NumberFormat(u"Section (\x0000" u".\x0001" u")");
list->get_ListLevels()->idx_get(1)->set_NumberStyle(Aspose::Words::NumberStyle::LeadingZero);

// Observera att den högre nivån använder UppercaseLetter-numrering.
// Vi kan ställa in egenskapen "IsLegal" för att använda arabiska siffror för de högre listnivåerna.
list->get_ListLevels()->idx_get(1)->set_IsLegal(true);
list->get_ListLevels()->idx_get(1)->set_RestartAfterLevel(0);

// Etiketter på nivå 3 kommer att vara stora romerska siffror med ett prefix och ett suffix och startar om vid varje List-nivå-1-objekt.
// Dessa listetiketter kommer att se ut som "-I-", "-II-"...
list->get_ListLevels()->idx_get(2)->set_NumberFormat(u"-\x0002" u"-");
list->get_ListLevels()->idx_get(2)->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
list->get_ListLevels()->idx_get(2)->set_RestartAfterLevel(1);

// Gör etiketter på alla listnivåer fetstilta.
for (auto&& level : list->get_ListLevels())
{
    level->get_Font()->set_Bold(true);
}

// Applicera listformatering på det aktuella stycket.
builder->get_ListFormat()->set_List(list);

// Skapa listobjekt som visar alla tre av våra listnivåer.
for (int32_t n = 0; n < 2; n++)
{
    for (int32_t i = 0; i < 3; i++)
    {
        builder->get_ListFormat()->set_ListLevelNumber(i);
        builder->Writeln(System::String(u"Level ") + i);
    }
}

builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.CreateListRestartAfterHigher.docx");
```

## Se även

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
