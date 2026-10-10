---
title: "Aspose::Words::Markup::SdtType enum"
linktitle: "SdtType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::SdtType enum. Specifica il tipo di nodo di un tag di documento strutturato (SDT) in C++."
type: docs
weight: 21000
url: /it/cpp/aspose.words.markup/sdttype/
---
## SdtType enum


Specifica il tipo di nodo di un tag di documento strutturato (SDT).

```cpp
enum class SdtType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Nessun tipo è assegnato al SDT. |
| Bibliografia | 1 | Il SDT rappresenta una voce di bibliografia. |
| Citazione | 2 | Il SDT rappresenta una citazione. |
| Equazione | 3 | Il SDT rappresenta un'equazione. |
| DropDownList | 4 | L'SDT rappresenta un elenco a discesa quando visualizzato nel documento. |
| ComboBox | 5 | L'SDT rappresenta una casella combinata quando visualizzata nel documento. |
| Data | 6 | L'SDT rappresenta un selettore di data quando visualizzato nel documento. |
| BuildingBlockGallery | 7 | L'SDT rappresenta un tipo di galleria di blocchi di costruzione. |
| DocPartObj | 8 | L'SDT rappresenta un tipo di parte del documento. |
| Group | 9 | L'SDT rappresenta un raggruppamento limitato quando visualizzato nel documento. |
| Picture | 10 | L'SDT rappresenta un'immagine quando visualizzata nel documento. |
| RichText | 11 | L'SDT rappresenta una casella di testo formattato quando visualizzata nel documento. |
| PlainText | 12 | L'SDT rappresenta una casella di testo semplice quando visualizzata nel documento. |
| Checkbox | 13 | L'SDT rappresenta una casella di controllo quando visualizzata nel documento. |
| RepeatingSection | 14 | L'SDT rappresenta il tipo di sezione ripetuta quando visualizzato nel documento. |
| RepeatingSectionItem | 15 | L'SDT rappresenta un elemento di sezione ripetuta. |
| EntityPicker | 16 | L'SDT rappresenta un selettore di entità che consente all'utente di selezionare un'istanza di un tipo di contenuto esterno. |


## Esempi



Mostra come lavorare con gli stili per gli elementi di controllo del contenuto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Di seguito sono riportati due modi per applicare uno stile dal documento a un tag di documento strutturato.
// 1 -  Applica un oggetto stile dalla collezione di stili del documento:
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Riferisci uno stile nel documento per nome:
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


Mostra come riempire una tabella con i dati da una parte XML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(u"Books", System::String(u"<books>") + u"<book>" + u"<title>Everyday Italian</title>" + u"<author>Giada De Laurentiis</author>" + u"</book>" + u"<book>" + u"<title>The C Programming Language</title>" + u"<author>Brian W. Kernighan, Dennis M. Ritchie</author>" + u"</book>" + u"<book>" + u"<title>Learning XML</title>" + u"<author>Erik T. Ray</author>" + u"</book>" + u"</books>");

// Crea intestazioni per i dati dal contenuto XML.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Title");
builder->InsertCell();
builder->Write(u"Author");
builder->EndRow();
builder->EndTable();

// Crea una tabella con una sezione ripetuta al suo interno.
auto repeatingSectionSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RepeatingSection, Aspose::Words::Markup::MarkupLevel::Row);
repeatingSectionSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book", System::String::Empty);
table->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(repeatingSectionSdt);

// Aggiungi un elemento di sezione ripetuta all'interno della sezione ripetuta e contrassegnalo come una riga.
// Questa tabella avrà una riga per ogni elemento che possiamo trovare nel documento XML
// utilizzando l'XPath "/books[1]/book", di cui ce ne sono tre.
auto repeatingSectionItemSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RepeatingSectionItem, Aspose::Words::Markup::MarkupLevel::Row);
repeatingSectionSdt->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(repeatingSectionItemSdt);

auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
repeatingSectionItemSdt->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

// Mappa i dati XML con le celle della tabella create per il titolo e l'autore di ogni libro.
auto titleSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Cell);
titleSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book[1]/title[1]", System::String::Empty);
row->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(titleSdt);

auto authorSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Cell);
authorSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book[1]/author[1]", System::String::Empty);
row->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(authorSdt);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.RepeatingSectionItem.docx");
```


Mostra come creare un tag di documento strutturato di gruppo a livello di riga.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Crea un tag di documento strutturato di gruppo a livello di riga.
auto groupSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Group, Aspose::Words::Markup::MarkupLevel::Row);
table->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(groupSdt);
groupSdt->set_IsShowingPlaceholderText(false);
groupSdt->RemoveAllChildren();

// Crea una riga figlia del tag di documento strutturato.
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
groupSdt->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

auto cell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
row->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(cell);

builder->EndTable();

// Inserisci il contenuto delle celle.
cell->EnsureMinimum();
builder->MoveTo(cell->get_LastParagraph());
builder->Write(u"Lorem ipsum dolor.");

// Inserisci il testo dopo la tabella.
builder->MoveTo(table->get_NextSibling());
builder->Write(u"Nulla blandit nisi.");

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.SdtAtRowLevel.docx");
```


Mostra come creare un tag di documento strutturato di tipo Citazione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto sdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Citation, Aspose::Words::Markup::MarkupLevel::Inline);
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(sdt);

// Crea un campo Citazione.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToParagraph(0, -1);
builder->InsertField(u"CITATION Ath22 \\l 1033 ", u"(John Lennon, 2022)");

// Sposta il campo nel tag di documento strutturato.
while (sdt->get_NextSibling() != nullptr)
{
    sdt->AppendChild<System::SharedPtr<Aspose::Words::Node>>(sdt->get_NextSibling());
}

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Citation.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
