---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_PlaceholderName metodo"
linktitle: "get_PlaceholderName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_PlaceholderName metodo. Ottiene o imposta il Nome del BuildingBlock contenente il testo segnaposto in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.markup/istructureddocumenttag/get_placeholdername/
---
## IStructuredDocumentTag::get_PlaceholderName method


Ottiene o imposta il Nome del [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) contenente il testo segnaposto.

```cpp
virtual System::String Aspose::Words::Markup::IStructuredDocumentTag::get_PlaceholderName()=0
```


## Esempi



Mostra come utilizzare il contenuto di un blocco di costruzione come testo segnaposto personalizzato per un tag di documento strutturato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Inserisci un tag di documento strutturato di testo semplice del tipo "PlainText", che funzionerà come una casella di testo.
// Il contenuto che visualizzerà per impostazione predefinita è il prompt "Click here to enter text.".
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Possiamo far visualizzare al tag il contenuto di un blocco di costruzione invece del testo predefinito.
// Per prima cosa, aggiungi un blocco di costruzione con contenuto al documento glossario.
System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossaryDoc = doc->get_GlossaryDocument();

auto substituteBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(glossaryDoc);
substituteBlock->set_Name(u"Custom Placeholder");
substituteBlock->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(glossaryDoc));
substituteBlock->get_FirstSection()->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(glossaryDoc));
substituteBlock->get_FirstSection()->get_Body()->AppendParagraph(u"Custom placeholder text.");

glossaryDoc->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(substituteBlock);

// Quindi, utilizza la proprietà "PlaceholderName" del tag di documento strutturato per fare riferimento a quel blocco di costruzione per nome.
tag->set_PlaceholderName(u"Custom Placeholder");

// Se "PlaceholderName" fa riferimento a un blocco esistente nel documento glossario del documento principale,
// potremo verificare il blocco di costruzione tramite la proprietà "Placeholder".
ASPOSE_ASSERT_EQ(substituteBlock, tag->get_Placeholder());

// Imposta la proprietà "IsShowingPlaceholderText" su "true" per trattare il
// contenuto corrente del tag di documento strutturato come testo segnaposto.
// Ciò significa che facendo clic sulla casella di testo in Microsoft Word verranno evidenziati immediatamente tutti i contenuti del tag.
// Imposta la proprietà "IsShowingPlaceholderText" su "false" per far sì che il
// tag di documento strutturato tratti il suo contenuto come testo già inserito dall'utente.
// Facendo clic su questo testo in Microsoft Word verrà posizionato il cursore lampeggiante nella posizione cliccata.
tag->set_IsShowingPlaceholderText(isShowingPlaceholderText);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

## Vedi anche

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
