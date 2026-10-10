---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_PlaceholderName Methode"
linktitle: "get_PlaceholderName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_PlaceholderName Methode. Liest oder setzt den Namen des BuildingBlock, das Platzhaltertext enthält, in C++."
type: docs
weight: 27000
url: /de/cpp/aspose.words.markup/structureddocumenttag/get_placeholdername/
---
## StructuredDocumentTag::get_PlaceholderName method


Liest oder schreibt den Namen des [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/), das Platzhaltertext enthält.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_PlaceholderName() override
```


## Beispiele



Zeigt, wie der Inhalt eines BuildingBlock als benutzerdefinierter Platzhaltertext für einen strukturierten Dokument-Tag verwendet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Fügen Sie einen strukturierten Dokument-Tag vom Typ "PlainText" ein, der als Textfeld fungiert.
// Der Inhalt, den es standardmäßig anzeigt, ist die Eingabeaufforderung "Klicken Sie hier, um Text einzugeben."
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Wir können den Tag dazu bringen, den Inhalt eines BuildingBlock anstelle des Standardtexts anzuzeigen.
// Fügen Sie zunächst einen BuildingBlock mit Inhalt zum Glossar-Dokument hinzu.
System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossaryDoc = doc->get_GlossaryDocument();

auto substituteBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(glossaryDoc);
substituteBlock->set_Name(u"Custom Placeholder");
substituteBlock->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(glossaryDoc));
substituteBlock->get_FirstSection()->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(glossaryDoc));
substituteBlock->get_FirstSection()->get_Body()->AppendParagraph(u"Custom placeholder text.");

glossaryDoc->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(substituteBlock);

// Verwenden Sie dann die "PlaceholderName"-Eigenschaft des strukturierten Dokument-Tags, um diesen BuildingBlock per Name zu referenzieren.
tag->set_PlaceholderName(u"Custom Placeholder");

// Wenn "PlaceholderName" auf einen vorhandenen Block im Glossar-Dokument des übergeordneten Dokuments verweist,
// können wir den BuildingBlock über die "Placeholder"-Eigenschaft überprüfen.
ASPOSE_ASSERT_EQ(substituteBlock, tag->get_Placeholder());

// Setzen Sie die "IsShowingPlaceholderText"-Eigenschaft auf "true", um das
// aktuelle Inhalt des strukturierten Dokument-Tags als Platzhaltertext zu behandeln.
// Das bedeutet, dass ein Klick auf das Textfeld in Microsoft Word sofort den gesamten Inhalt des Tags hervorhebt.
// Setzen Sie die "IsShowingPlaceholderText"-Eigenschaft auf "false", um das
// Strukturiertes Dokumentensteuerelement, damit es seinen Inhalt als Text behandelt, den ein Benutzer bereits eingegeben hat.
// Ein Klick auf diesen Text in Microsoft Word positioniert den blinkenden Cursor an der angeklickten Stelle.
tag->set_IsShowingPlaceholderText(isShowingPlaceholderText);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

## Siehe auch

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
