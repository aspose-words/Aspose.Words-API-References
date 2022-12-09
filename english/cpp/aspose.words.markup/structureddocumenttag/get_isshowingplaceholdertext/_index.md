---
title: get_IsShowingPlaceholderText
second_title: Aspose.Words for C++ API Reference
description: Specifies whether the content of this SDT shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). if set to true, this state shall be resumed (showing placeholder text) upon opening this document.
type: docs
weight: 222
url: /cpp/aspose.words.markup/structureddocumenttag/get_isshowingplaceholdertext/
---
## StructuredDocumentTag::get_IsShowingPlaceholderText method


Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). if set to **true**, this state shall be resumed (showing placeholder text) upon opening this document.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_IsShowingPlaceholderText() override
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

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words](../../../)
