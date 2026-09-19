---
title: "Metodo Aspose::Words::Markup::StructuredDocumentTag::Clear"
linktitle: "Cancella"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Markup::StructuredDocumentTag::Clear. Cancella il contenuto di questo tag di documento strutturato e visualizza un segnaposto se è definito in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag::Clear method


Cancella il contenuto di questo tag di documento strutturato e visualizza un segnaposto se è definito.

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::Clear()
```

## Note


Non è possibile cancellare il contenuto di un tag di documento strutturato se contiene revisioni.

Se questo tag di documento strutturato è mappato a XML personalizzato (utilizzando la proprietà [XmlMapping](../get_xmlmapping/)), il nodo XML di riferimento viene cancellato.

## Esempi



Mostra come eliminare i contenuti degli elementi del tag di documento strutturato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Crea un tag di documento strutturato di testo semplice, quindi aggiungilo al documento.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

// Questo tag di documento strutturato, che ha la forma di una casella di testo, visualizza già il testo segnaposto.
ASSERT_EQ(u"Click here to enter text.", tag->GetText().Trim());
ASSERT_TRUE(tag->get_IsShowingPlaceholderText());

// Crea un blocco di costruzione con contenuti di testo.
System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossaryDoc = doc->get_GlossaryDocument();
auto substituteBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(glossaryDoc);
substituteBlock->set_Name(u"My placeholder");
substituteBlock->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(glossaryDoc));
substituteBlock->get_FirstSection()->EnsureMinimum();
substituteBlock->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(glossaryDoc, u"Custom placeholder text."));
glossaryDoc->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(substituteBlock);

// Imposta la proprietà "PlaceholderName" del tag di documento strutturato al nome del nostro blocco di costruzione per ottenere
// che il tag di documento strutturato visualizzi i contenuti del blocco di costruzione al posto del testo predefinito originale.
tag->set_PlaceholderName(u"My placeholder");

ASSERT_EQ(u"Custom placeholder text.", tag->GetText().Trim());
ASSERT_TRUE(tag->get_IsShowingPlaceholderText());

// Modifica il testo del tag di documento strutturato e nascondi il testo segnaposto.
auto run = System::ExplicitCast<Aspose::Words::Run>(tag->GetChild(Aspose::Words::NodeType::Run, 0, true));
run->set_Text(u"New text.");
tag->set_IsShowingPlaceholderText(false);

ASSERT_EQ(u"New text.", tag->GetText().Trim());

// Usa il metodo "Clear" per cancellare i contenuti di questo tag di documento strutturato e visualizzare nuovamente il segnaposto.
tag->Clear();

ASSERT_TRUE(tag->get_IsShowingPlaceholderText());
ASSERT_EQ(u"Custom placeholder text.", tag->GetText().Trim());
```

## Vedi anche

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
