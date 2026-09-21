---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_Placeholder metod"
linktitle: "get_Placeholder"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_Placeholder metod. Hämtar BuildingBlock som innehåller platshållartext som ska visas när innehållet i detta SDT-kör är tomt, det associerade mappade XML-elementet är tomt enligt XmlMapping-elementet eller när IsShowingPlaceholderText-elementet är sant i C++."
type: docs
weight: 26000
url: /sv/cpp/aspose.words.markup/structureddocumenttag/get_placeholder/
---
## StructuredDocumentTag::get_Placeholder method


Hämtar [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) som innehåller platshållartext som ska visas när innehållet i detta SDT-kör är tomt, det associerade mappade XML-elementet är tomt enligt [XmlMapping](../get_xmlmapping/)-elementet eller när [IsShowingPlaceholderText](../get_isshowingplaceholdertext/)-elementet är **true**.

```cpp
System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> Aspose::Words::Markup::StructuredDocumentTag::get_Placeholder() override
```


## Exempel



Visar hur man använder innehållet i ett byggblock som anpassad platshållartext för en strukturerad dokumenttagg.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Infoga en strukturerad dokumenttagg med ren text av typen "PlainText", som kommer att fungera som en textruta.
// Innehållet som den kommer att visa som standard är en uppmaning "Click here to enter text.".
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Vi kan få taggen att visa innehållet i ett byggblock istället för standardtexten.
// Först, lägg till ett byggblock med innehåll i glossariedokumentet.
System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossaryDoc = doc->get_GlossaryDocument();

auto substituteBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(glossaryDoc);
substituteBlock->set_Name(u"Custom Placeholder");
substituteBlock->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(glossaryDoc));
substituteBlock->get_FirstSection()->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(glossaryDoc));
substituteBlock->get_FirstSection()->get_Body()->AppendParagraph(u"Custom placeholder text.");

glossaryDoc->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(substituteBlock);

// Sedan, använd den strukturerade dokumenttaggens egenskap "PlaceholderName" för att referera till det byggblocket med namn.
tag->set_PlaceholderName(u"Custom Placeholder");

// Om "PlaceholderName" refererar till ett befintligt block i förälderdokumentets glossariedokument,
// kommer vi att kunna verifiera byggblocket via egenskapen "Placeholder".
ASPOSE_ASSERT_EQ(substituteBlock, tag->get_Placeholder());

// Ställ in egenskapen "IsShowingPlaceholderText" till "true" för att behandla
// den strukturerade dokumenttaggens aktuella innehåll som platshållartext.
// Detta betyder att ett klick på textrutan i Microsoft Word omedelbart markerar allt taggens innehåll.
// Ställ in egenskapen "IsShowingPlaceholderText" till "false" för att få
// den strukturerade dokumenttaggen att behandla dess innehåll som text som en användare redan har skrivit in.
// Att klicka på den här texten i Microsoft Word placerar den blinkande markören på den klickade platsen.
tag->set_IsShowingPlaceholderText(isShowingPlaceholderText);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

## Se även

* Class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
