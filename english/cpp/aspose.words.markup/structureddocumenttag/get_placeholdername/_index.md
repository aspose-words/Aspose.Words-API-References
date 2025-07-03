---
title: Aspose::Words::Markup::StructuredDocumentTag::get_PlaceholderName method
linktitle: get_PlaceholderName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTag::get_PlaceholderName method. Gets or sets Name of the BuildingBlock containing placeholder text in C++.'
type: docs
weight: 27000
url: /cpp/aspose.words.markup/structureddocumenttag/get_placeholdername/
---
## StructuredDocumentTag::get_PlaceholderName method


Gets or sets Name of the [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) containing placeholder text.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_PlaceholderName() override
```


## Examples



Shows how to use a building block's contents as a custom placeholder text for a structured document tag. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Insert a plain text structured document tag of the "PlainText" type, which will function as a text box.
// The contents that it will display by default are a "Click here to enter text." prompt.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// We can get the tag to display the contents of a building block instead of the default text.
// First, add a building block with contents to the glossary document.
System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossaryDoc = doc->get_GlossaryDocument();

auto substituteBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(glossaryDoc);
substituteBlock->set_Name(u"Custom Placeholder");
substituteBlock->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(glossaryDoc));
substituteBlock->get_FirstSection()->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(glossaryDoc));
substituteBlock->get_FirstSection()->get_Body()->AppendParagraph(u"Custom placeholder text.");

glossaryDoc->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(substituteBlock);

// Then, use the structured document tag's "PlaceholderName" property to reference that building block by name.
tag->set_PlaceholderName(u"Custom Placeholder");

// If "PlaceholderName" refers to an existing block in the parent document's glossary document,
// we will be able to verify the building block via the "Placeholder" property.
ASPOSE_ASSERT_EQ(substituteBlock, tag->get_Placeholder());

// Set the "IsShowingPlaceholderText" property to "true" to treat the
// structured document tag's current contents as placeholder text.
// This means that clicking on the text box in Microsoft Word will immediately highlight all the tag's contents.
// Set the "IsShowingPlaceholderText" property to "false" to get the
// structured document tag to treat its contents as text that a user has already entered.
// Clicking on this text in Microsoft Word will place the blinking cursor at the clicked location.
tag->set_IsShowingPlaceholderText(isShowingPlaceholderText);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

## See Also

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
