---
title: "Aspose::Words::Lists::ListFormat::RemoveNumbers method"
linktitle: "RemoveNumbers"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Lists::ListFormat::RemoveNumbers‑metod. Tar bort siffror eller punkter från det aktuella stycket och sätter listnivån till noll i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words.lists/listformat/removenumbers/
---
## ListFormat::RemoveNumbers method


Tar bort siffror eller punkter från det aktuella stycket och sätter listnivån till noll.

```cpp
void Aspose::Words::Lists::ListFormat::RemoveNumbers()
```

## Anmärkningar


Att anropa den här metoden är likvärdigt med att sätta egenskapen [List](../get_list/) till **null**.

## Exempel



Visar hur man skapar punkt- och numrerade listor.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Aspose.Words main advantages are:");

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
// Vi kan skapa nästlade listor genom att öka indragnivån.
// Vi kan börja och avsluta en lista genom att använda en dokumentbyggares egenskap "ListFormat".
// Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
// Nedan är två typer av listor som vi kan skapa med en dokumentbyggare.
// 1 -  En punktlista:
// Denna lista kommer att applicera ett indrag och en punktsymbol ("•") före varje stycke.
builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Great performance");
builder->Writeln(u"High reliability");
builder->Writeln(u"Quality code and working");
builder->Writeln(u"Wide variety of features");
builder->Writeln(u"Easy to understand API");

// Avsluta punktlistan.
builder->get_ListFormat()->RemoveNumbers();

builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->Writeln(u"Aspose.Words allows:");

// 2 -  En numrerad lista:
// Numrerade listor skapar en logisk ordning för sina stycken genom att numrera varje objekt.
builder->get_ListFormat()->ApplyNumberDefault();

// Detta stycke är det första objektet. Det första objektet i en numrerad lista kommer att ha ett "1." som listobjektsymbol.
builder->Writeln(u"Opening documents from different formats:");

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// Anropa "ListIndent"‑metoden för att öka den aktuella listnivån,
// vilket kommer att starta en ny självständig lista, med ett djupare indrag, vid det aktuella objektet på den första listnivån.
builder->get_ListFormat()->ListIndent();

ASSERT_EQ(1, builder->get_ListFormat()->get_ListLevelNumber());

// Detta är de första tre listobjekten på den andra listnivån, som kommer att behålla en räknare
// oberoende av antalet i den första listnivån. Enligt det aktuella listformatet,
// de kommer att ha symbolerna "a.", "b.", och "c.".
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");

// Anropa metoden "ListOutdent" för att återgå till föregående listnivå.
builder->get_ListFormat()->ListOutdent();

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// Dessa två stycken kommer att fortsätta räkningen av den första listnivån.
// Dessa objekt kommer att ha symbolerna "2.", och "3."
builder->Writeln(u"Processing documents");
builder->Writeln(u"Saving documents in different formats:");

// Om vi ökar listnivån till en nivå som vi tidigare har lagt till objekt på,
// kommer den nästlade listan att vara separat från den föregående, och dess numrering kommer att börja från början.
// Dessa listobjekt kommer att ha symbolerna "a.", "b.", "c.", "d.", och "e".
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");
builder->Writeln(u"MHTML");
builder->Writeln(u"Plain text");

// Minska indraget för listnivån igen.
builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"Doing many other things!");

// Avsluta den numrerade listan.
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.ApplyDefaultBulletsAndNumbers.docx");
```


Visar hur man tar bort listformatering från alla stycken i huvudtexten i ett avsnitt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");
builder->Writeln(u"Numbered list item 3");
builder->get_ListFormat()->RemoveNumbers();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);
ASSERT_EQ(3, paras->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Paragraph>(n))->get_ListFormat()->get_IsListItem();
}))));

for (auto&& paragraph : System::IterateOver<Aspose::Words::Paragraph>(paras))
{
    paragraph->get_ListFormat()->RemoveNumbers();
}

ASSERT_EQ(0, paras->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Paragraph>(n))->get_ListFormat()->get_IsListItem();
}))));
```

## Se även

* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
