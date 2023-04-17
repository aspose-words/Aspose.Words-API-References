---
title: Aspose::Words::Markup::StructuredDocumentTag::Clear method
linktitle: Clear
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTag::Clear method. Clears contents of this structured document tag and displays a placeholder if it is defined in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag::Clear method


Clears contents of this structured document tag and displays a placeholder if it is defined.

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::Clear()
```

## Remarks


It is not possible to clear contents of a structured document tag if it has revisions.

If this structured document tag is mapped to custom XML (with using the [XmlMapping](../get_xmlmapping/) property), the referenced XML node is cleared.

## Examples



Shows how to delete contents of structured document tag elements. 
```cpp
auto doc = MakeObject<Document>();

// Create a plain text structured document tag, and then append it to the document.
auto tag = MakeObject<StructuredDocumentTag>(doc, SdtType::PlainText, MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild(tag);

// This structured document tag, which is in the form of a text box, already displays placeholder text.
ASSERT_EQ(u"Click here to enter text.", tag->GetText().Trim());
ASSERT_TRUE(tag->get_IsShowingPlaceholderText());

// Create a building block with text contents.
SharedPtr<GlossaryDocument> glossaryDoc = doc->get_GlossaryDocument();
auto substituteBlock = MakeObject<BuildingBlock>(glossaryDoc);
substituteBlock->set_Name(u"My placeholder");
substituteBlock->AppendChild(MakeObject<Section>(glossaryDoc));
substituteBlock->get_FirstSection()->EnsureMinimum();
substituteBlock->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(MakeObject<Run>(glossaryDoc, u"Custom placeholder text."));
glossaryDoc->AppendChild(substituteBlock);

// Set the structured document tag's "PlaceholderName" property to our building block's name to get
// the structured document tag to display the contents of the building block in place of the original default text.
tag->set_PlaceholderName(u"My placeholder");

ASSERT_EQ(u"Custom placeholder text.", tag->GetText().Trim());
ASSERT_TRUE(tag->get_IsShowingPlaceholderText());

// Edit the text of the structured document tag and hide the placeholder text.
auto run = System::DynamicCast<Run>(tag->GetChild(NodeType::Run, 0, true));
run->set_Text(u"New text.");
tag->set_IsShowingPlaceholderText(false);

ASSERT_EQ(u"New text.", tag->GetText().Trim());

// Use the "Clear" method to clear this structured document tag's contents and display the placeholder again.
tag->Clear();

ASSERT_TRUE(tag->get_IsShowingPlaceholderText());
ASSERT_EQ(u"Custom placeholder text.", tag->GetText().Trim());
```

## See Also

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
