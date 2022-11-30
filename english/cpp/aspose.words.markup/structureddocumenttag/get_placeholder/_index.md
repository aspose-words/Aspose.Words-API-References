---
title: get_Placeholder
second_title: Aspose.Words for C++ API Reference
description: Gets the BuildingBlock containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the XmlMapping element or the IsShowingPlaceholderText element is true.
type: docs
weight: 313
url: /cpp/aspose.words.markup/structureddocumenttag/get_placeholder/
---
## StructuredDocumentTag::get_Placeholder method


Gets the [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [XmlMapping](../get_xmlmapping/) element or the [IsShowingPlaceholderText](../get_isshowingplaceholdertext/) element is true.

```cpp
System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> Aspose::Words::Markup::StructuredDocumentTag::get_Placeholder() override
```


## Examples



Shows how to use a building block's contents as a custom placeholder text for a structured document tag. 
```cpp
auto doc = MakeObject<Document>();

// Insert a plain text structured document tag of the "PlainText" type, which will function as a text box.
// The contents that it will display by default are a "Click here to enter text." prompt.
auto tag = MakeObject<StructuredDocumentTag>(doc, SdtType::PlainText, MarkupLevel::Inline);

// We can get the tag to display the contents of a building block instead of the default text.
// First, add a building block with contents to the glossary document.
SharedPtr<GlossaryDocument> glossaryDoc = doc->get_GlossaryDocument();

auto substituteBlock = MakeObject<BuildingBlock>(glossaryDoc);
substituteBlock->set_Name(u"Custom Placeholder");
substituteBlock->AppendChild(MakeObject<Section>(glossaryDoc));
substituteBlock->get_FirstSection()->AppendChild(MakeObject<Body>(glossaryDoc));
substituteBlock->get_FirstSection()->get_Body()->AppendParagraph(u"Custom placeholder text.");

glossaryDoc->AppendChild(substituteBlock);

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

auto builder = MakeObject<DocumentBuilder>(doc);
builder->InsertNode(tag);

doc->Save(ArtifactsDir + u"StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

## See Also

* Class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words](../../../)
