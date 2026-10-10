---
title: "Aspose::Words::Markup::SdtType enum"
linktitle: "SdtType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::SdtType enum. Gibt den Typ eines strukturierten Dokumenten‑Tags (SDT)‑Knotens in C++ an."
type: docs
weight: 21000
url: /de/cpp/aspose.words.markup/sdttype/
---
## SdtType enum


Gibt den Typ eines strukturierten Dokument‑Tag‑Knotens (SDT) an.

```cpp
enum class SdtType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 | Der SDT hat keinen zugewiesenen Typ. |
| Bibliografie | 1 | Der SDT stellt einen Bibliografieeintrag dar. |
| Zitat | 2 | Der SDT stellt ein Zitat dar. |
| Gleichung | 3 | Der SDT stellt eine Gleichung dar. |
| DropDownList | 4 | Der SDT stellt eine Dropdown-Liste dar, wenn er im Dokument angezeigt wird. |
| ComboBox | 5 | Der SDT stellt ein Kombinationsfeld dar, wenn er im Dokument angezeigt wird. |
| Datum | 6 | Der SDT stellt einen Datumswähler dar, wenn er im Dokument angezeigt wird. |
| BuildingBlockGallery | 7 | Der SDT stellt einen Baustein-Galerietyp dar. |
| DocPartObj | 8 | Der SDT stellt einen Dokumentteiltyp dar. |
| Gruppe | 9 | Der SDT stellt eine eingeschränkte Gruppierung dar, wenn er im Dokument angezeigt wird. |
| Bild | 10 | Der SDT stellt ein Bild dar, wenn er im Dokument angezeigt wird. |
| RichText | 11 | Der SDT stellt ein Rich‑Text‑Feld dar, wenn er im Dokument angezeigt wird. |
| PlainText | 12 | Der SDT stellt ein einfaches Textfeld dar, wenn er im Dokument angezeigt wird. |
| Kontrollkästchen | 13 | Das SDT stellt ein Kontrollkästchen dar, wenn es im Dokument angezeigt wird. |
| RepeatingSection | 14 | Das SDT stellt den Wiederholungsabschnittstyp dar, wenn es im Dokument angezeigt wird. |
| RepeatingSectionItem | 15 | Das SDT stellt ein Wiederholungsabschnittselement dar. |
| EntityPicker | 16 | Das SDT stellt einen EntityPicker dar, der es dem Benutzer ermöglicht, eine Instanz eines externen Inhaltstyps auszuwählen. |


## Beispiele



Zeigt, wie man mit Stilen für Content-Control-Elemente arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Unten sind zwei Möglichkeiten aufgeführt, einen Stil aus dem Dokument auf ein strukturiertes Dokument-Tag anzuwenden.
// 1 -  Wende ein Stilobjekt aus der Stilsammlung des Dokuments an:
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Verweise im Dokument per Name auf einen Stil:
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


Zeigt, wie man eine Tabelle mit Daten aus einem XML-Teil füllt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(u"Books", System::String(u"<books>") + u"<book>" + u"<title>Everyday Italian</title>" + u"<author>Giada De Laurentiis</author>" + u"</book>" + u"<book>" + u"<title>The C Programming Language</title>" + u"<author>Brian W. Kernighan, Dennis M. Ritchie</author>" + u"</book>" + u"<book>" + u"<title>Learning XML</title>" + u"<author>Erik T. Ray</author>" + u"</book>" + u"</books>");

// Erstelle Kopfzeilen für Daten aus dem XML-Inhalt.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Title");
builder->InsertCell();
builder->Write(u"Author");
builder->EndRow();
builder->EndTable();

// Erstelle eine Tabelle mit einem wiederholenden Abschnitt darin.
auto repeatingSectionSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RepeatingSection, Aspose::Words::Markup::MarkupLevel::Row);
repeatingSectionSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book", System::String::Empty);
table->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(repeatingSectionSdt);

// Füge ein Wiederholungsabschnittselement innerhalb des Wiederholungsabschnitts hinzu und markiere es als Zeile.
// Diese Tabelle wird für jedes Element, das wir im XML-Dokument finden, eine Zeile enthalten.
// unter Verwendung des XPath \"/books[1]/book\", von denen es drei gibt.
auto repeatingSectionItemSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RepeatingSectionItem, Aspose::Words::Markup::MarkupLevel::Row);
repeatingSectionSdt->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(repeatingSectionItemSdt);

auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
repeatingSectionItemSdt->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

// Ordne XML-Daten den erstellten Tabellenspalten für den Titel und den Autor jedes Buches zu.
auto titleSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Cell);
titleSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book[1]/title[1]", System::String::Empty);
row->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(titleSdt);

auto authorSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Cell);
authorSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book[1]/author[1]", System::String::Empty);
row->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(authorSdt);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.RepeatingSectionItem.docx");
```


Zeigt, wie man ein Group structured document tag auf Zeilenebene erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Erstelle ein Group structured document tag auf Zeilenebene.
auto groupSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Group, Aspose::Words::Markup::MarkupLevel::Row);
table->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(groupSdt);
groupSdt->set_IsShowingPlaceholderText(false);
groupSdt->RemoveAllChildren();

// Erstelle eine untergeordnete Zeile des strukturierten Dokument-Tags.
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
groupSdt->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

auto cell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
row->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(cell);

builder->EndTable();

// Füge Zelleninhalte ein.
cell->EnsureMinimum();
builder->MoveTo(cell->get_LastParagraph());
builder->Write(u"Lorem ipsum dolor.");

// Füge Text nach der Tabelle ein.
builder->MoveTo(table->get_NextSibling());
builder->Write(u"Nulla blandit nisi.");

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.SdtAtRowLevel.docx");
```


Zeigt, wie man ein strukturiertes Dokument-Tag vom Typ Citation erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto sdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Citation, Aspose::Words::Markup::MarkupLevel::Inline);
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(sdt);

// Erstelle ein Citation-Feld.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToParagraph(0, -1);
builder->InsertField(u"CITATION Ath22 \\l 1033 ", u"(John Lennon, 2022)");

// Verschiebe das Feld zum strukturierten Dokument-Tag.
while (sdt->get_NextSibling() != nullptr)
{
    sdt->AppendChild<System::SharedPtr<Aspose::Words::Node>>(sdt->get_NextSibling());
}

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Citation.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
