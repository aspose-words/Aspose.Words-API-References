---
title: "Aspose::Words::Markup::SdtType enum"
linktitle: "SdtType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::SdtType enum. Anger typen av en strukturerad dokumenttagg (SDT) nod i C++."
type: docs
weight: 21000
url: /sv/cpp/aspose.words.markup/sdttype/
---
## SdtType enum


Anger typen av en strukturerad dokumenttagg (SDT)-nod.

```cpp
enum class SdtType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 | Ingen typ har tilldelats SDT:n. |
| Bibliografi | 1 | SDT:n representerar en bibliografipost. |
| Citat | 2 | SDT:n representerar ett citat. |
| Ekvation | 3 | SDT:n representerar en ekvation. |
| Rullgardinslista | 4 | SDT:n representerar en rullgardinslista när den visas i dokumentet. |
| Kombinationsruta | 5 | SDT:n representerar en kombinationsruta när den visas i dokumentet. |
| Datum | 6 | SDT:n representerar en datumväljare när den visas i dokumentet. |
| BuildingBlockGallery | 7 | SDT:n representerar en byggblocksgalleri-typ. |
| DocPartObj | 8 | SDT:n representerar en dokumentdelstyp. |
| Grupp | 9 | SDT:n representerar en begränsad gruppering när den visas i dokumentet. |
| Bild | 10 | SDT:n representerar en bild när den visas i dokumentet. |
| RichText | 11 | SDT:n representerar en rich text-ruta när den visas i dokumentet. |
| PlainText | 12 | SDT representerar en vanlig textruta när den visas i dokumentet. |
| Kryssruta | 13 | SDT representerar en kryssruta när den visas i dokumentet. |
| RepeatingSection | 14 | SDT representerar en upprepande sektionstyp när den visas i dokumentet. |
| RepeatingSectionItem | 15 | SDT representerar ett upprepande sektionselement. |
| EntityPicker | 16 | SDT representerar en entity picker som tillåter användaren att välja en instans av en extern innehållstyp. |


## Exempel



Visar hur man arbetar med stilar för innehållskontrollelement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nedan följer två sätt att applicera en stil från dokumentet på en strukturerad dokumenttagg.
// 1 -  Applicera ett stilobjekt från dokumentets stilkollektion:
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Referera till en stil i dokumentet med namn:
auto sdtRichText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtRichText->set_StyleName(u"Quote");

builder->InsertNode(sdtPlainText);
builder->InsertNode(sdtRichText);

ASSERT_EQ(Aspose::Words::NodeType::StructuredDocumentTag, sdtPlainText->get_NodeType());

System::SharedPtr<Aspose::Words::NodeCollection> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

for (auto&& node : System::IterateOver(tags))
{
    auto sdt = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(node);

    std::cout << sdt->get_WordOpenXMLMinimal() << std::endl;

    ASSERT_EQ(Aspose::Words::StyleIdentifier::Quote, sdt->get_Style()->get_StyleIdentifier());
    ASSERT_EQ(u"Quote", sdt->get_StyleName());
}
```


Visar hur man fyller en tabell med data från en XML-del.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(u"Books", System::String(u"<books>") + u"<book>" + u"<title>Everyday Italian</title>" + u"<author>Giada De Laurentiis</author>" + u"</book>" + u"<book>" + u"<title>The C Programming Language</title>" + u"<author>Brian W. Kernighan, Dennis M. Ritchie</author>" + u"</book>" + u"<book>" + u"<title>Learning XML</title>" + u"<author>Erik T. Ray</author>" + u"</book>" + u"</books>");

// Skapa rubriker för data från XML-innehållet.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Title");
builder->InsertCell();
builder->Write(u"Author");
builder->EndRow();
builder->EndTable();

// Skapa en tabell med en upprepande sektion inuti.
auto repeatingSectionSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RepeatingSection, Aspose::Words::Markup::MarkupLevel::Row);
repeatingSectionSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book", System::String::Empty);
table->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(repeatingSectionSdt);

// Lägg till ett upprepande sektionselement i den upprepande sektionen och markera det som en rad.
// Denna tabell kommer att ha en rad för varje element som vi kan hitta i XML-dokumentet.
// med XPath "/books[1]/book", varav det finns tre.
auto repeatingSectionItemSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RepeatingSectionItem, Aspose::Words::Markup::MarkupLevel::Row);
repeatingSectionSdt->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(repeatingSectionItemSdt);

auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
repeatingSectionItemSdt->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

// Mappa XML-data med skapade tabellceller för titeln och författaren för varje bok.
auto titleSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Cell);
titleSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book[1]/title[1]", System::String::Empty);
row->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(titleSdt);

auto authorSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Cell);
authorSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book[1]/author[1]", System::String::Empty);
row->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(authorSdt);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.RepeatingSectionItem.docx");
```


Visar hur man skapar en gruppstrukturerad dokumenttagg på radnivå.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Skapa en gruppstrukturerad dokumenttagg på radnivå.
auto groupSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Group, Aspose::Words::Markup::MarkupLevel::Row);
table->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(groupSdt);
groupSdt->set_IsShowingPlaceholderText(false);
groupSdt->RemoveAllChildren();

// Skapa en underordnad rad för den strukturerade dokumenttaggen.
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
groupSdt->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

auto cell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
row->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(cell);

builder->EndTable();

// Infoga cellinnehåll.
cell->EnsureMinimum();
builder->MoveTo(cell->get_LastParagraph());
builder->Write(u"Lorem ipsum dolor.");

// Infoga text efter tabellen.
builder->MoveTo(table->get_NextSibling());
builder->Write(u"Nulla blandit nisi.");

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.SdtAtRowLevel.docx");
```


Visar hur man skapar en strukturerad dokumenttagg av typen Citation.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto sdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Citation, Aspose::Words::Markup::MarkupLevel::Inline);
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(sdt);

// Skapa ett Citation-fält.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToParagraph(0, -1);
builder->InsertField(u"CITATION Ath22 \\l 1033 ", u"(John Lennon, 2022)");

// Flytta fältet till den strukturerade dokumenttaggen.
while (sdt->get_NextSibling() != nullptr)
{
    sdt->AppendChild<System::SharedPtr<Aspose::Words::Node>>(sdt->get_NextSibling());
}

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Citation.docx");
```

## Se även

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
