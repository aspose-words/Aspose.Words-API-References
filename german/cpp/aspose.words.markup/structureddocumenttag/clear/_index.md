---
title: "Aspose::Words::Markup::StructuredDocumentTag::Clear Methode"
linktitle: "Clear"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTag::Clear Methode. Löscht den Inhalt dieses strukturierten Dokumenttags und zeigt einen Platzhalter an, falls dieser in C++ definiert ist."
type: docs
weight: 4000
url: /de/cpp/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag::Clear method


Löscht den Inhalt dieses strukturierten Dokument‑Tags und zeigt einen Platzhalter an, falls er definiert ist.

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::Clear()
```

## Hinweise


Es ist nicht möglich, den Inhalt eines strukturierten Dokumenttags zu löschen, wenn er Revisionen enthält.

Wenn dieser strukturierte Dokumenttag mit benutzerdefiniertem XML (unter Verwendung der [XmlMapping](../get_xmlmapping/) Eigenschaft) verknüpft ist, wird der referenzierte XML-Knoten gelöscht.

## Beispiele



Zeigt, wie Inhalte von strukturierten Dokumenttag-Elementen gelöscht werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Erstellen Sie einen strukturierten Dokumenttag mit einfachem Text und fügen Sie ihn anschließend dem Dokument hinzu.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

// Dieser strukturierte Dokumenttag, der in Form einer Textbox vorliegt, zeigt bereits Platzhaltertext an.
ASSERT_EQ(u"Click here to enter text.", tag->GetText().Trim());
ASSERT_TRUE(tag->get_IsShowingPlaceholderText());

// Erstellen Sie einen Baustein mit Textinhalt.
System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossaryDoc = doc->get_GlossaryDocument();
auto substituteBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(glossaryDoc);
substituteBlock->set_Name(u"My placeholder");
substituteBlock->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(glossaryDoc));
substituteBlock->get_FirstSection()->EnsureMinimum();
substituteBlock->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(glossaryDoc, u"Custom placeholder text."));
glossaryDoc->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(substituteBlock);

// Setzen Sie die "PlaceholderName"-Eigenschaft des strukturierten Dokumenttags auf den Namen unseres Bausteins, um
// dass der strukturierte Dokumenttag den Inhalt des Bausteins anstelle des ursprünglichen Standardtexts anzeigt.
tag->set_PlaceholderName(u"My placeholder");

ASSERT_EQ(u"Custom placeholder text.", tag->GetText().Trim());
ASSERT_TRUE(tag->get_IsShowingPlaceholderText());

// Bearbeiten Sie den Text des strukturierten Dokumenttags und verbergen Sie den Platzhaltertext.
auto run = System::ExplicitCast<Aspose::Words::Run>(tag->GetChild(Aspose::Words::NodeType::Run, 0, true));
run->set_Text(u"New text.");
tag->set_IsShowingPlaceholderText(false);

ASSERT_EQ(u"New text.", tag->GetText().Trim());

// Verwenden Sie die Methode "Clear", um den Inhalt dieses strukturierten Dokumenttags zu löschen und den Platzhalter erneut anzuzeigen.
tag->Clear();

ASSERT_TRUE(tag->get_IsShowingPlaceholderText());
ASSERT_EQ(u"Custom placeholder text.", tag->GetText().Trim());
```

## Siehe auch

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
