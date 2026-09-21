---
title: "Aspose::Words::Markup::StructuredDocumentTag::Clear metod"
linktitle: "Clear"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::StructuredDocumentTag::Clear metod. Rensar innehållet i detta strukturerade dokumenttagg och visar en platshållare om den är definierad i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag::Clear method


Rensar innehållet i denna strukturerade dokumenttagg och visar en platshållare om den är definierad.

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::Clear()
```

## Anmärkningar


Det är inte möjligt att rensa innehållet i en strukturerad dokumenttagg om den har revisioner.

Om denna strukturerade dokumenttagg är mappad till anpassad XML (genom att använda egenskapen [XmlMapping](../get_xmlmapping/)), rensas den refererade XML-noden.

## Exempel



Visar hur man tar bort innehållet i element för strukturerade dokumenttaggar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Skapa en strukturerad dokumenttagg med vanlig text och lägg sedan till den i dokumentet.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

// Denna strukturerade dokumenttagg, som är i form av en textruta, visar redan platshållartext.
ASSERT_EQ(u"Click here to enter text.", tag->GetText().Trim());
ASSERT_TRUE(tag->get_IsShowingPlaceholderText());

// Skapa ett byggblock med textinnehåll.
System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossaryDoc = doc->get_GlossaryDocument();
auto substituteBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(glossaryDoc);
substituteBlock->set_Name(u"My placeholder");
substituteBlock->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(glossaryDoc));
substituteBlock->get_FirstSection()->EnsureMinimum();
substituteBlock->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(glossaryDoc, u"Custom placeholder text."));
glossaryDoc->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(substituteBlock);

// Ställ in strukturerade dokumenttaggens egenskap "PlaceholderName" till vårt byggblocks namn för att få
// den strukturerade dokumenttaggen att visa innehållet i byggblocket i stället för den ursprungliga standardtexten.
tag->set_PlaceholderName(u"My placeholder");

ASSERT_EQ(u"Custom placeholder text.", tag->GetText().Trim());
ASSERT_TRUE(tag->get_IsShowingPlaceholderText());

// Redigera texten i den strukturerade dokumenttaggen och dölj platshållartexten.
auto run = System::ExplicitCast<Aspose::Words::Run>(tag->GetChild(Aspose::Words::NodeType::Run, 0, true));
run->set_Text(u"New text.");
tag->set_IsShowingPlaceholderText(false);

ASSERT_EQ(u"New text.", tag->GetText().Trim());

// Använd metoden "Clear" för att rensa innehållet i denna strukturerade dokumenttagg och visa platshållaren igen.
tag->Clear();

ASSERT_TRUE(tag->get_IsShowingPlaceholderText());
ASSERT_EQ(u"Custom placeholder text.", tag->GetText().Trim());
```

## Se även

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
