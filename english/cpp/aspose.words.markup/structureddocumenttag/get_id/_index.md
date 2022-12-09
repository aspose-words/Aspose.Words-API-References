---
title: get_Id
second_title: Aspose.Words for C++ API Reference
description: Specifies a unique read-only persistent numerical Id for this SDT.
type: docs
weight: 209
url: /cpp/aspose.words.markup/structureddocumenttag/get_id/
---
## StructuredDocumentTag::get_Id method


Specifies a unique read-only persistent numerical Id for this **SDT**.

```cpp
int32_t Aspose::Words::Markup::StructuredDocumentTag::get_Id() override
```

## Remarks


Id attribute shall follow these rules:* The document shall retain SDT ids only if the whole document is cloned [Clone](../../../aspose.words/document/clone/).
* During [ImportNode()](../) Id shall be retained if import does not cause conflicts with other SDT Ids in the target document.
* If multiple SDT nodes specify the same decimal number value for the Id attribute, then the first SDT in the document shall maintain this original Id, and all subsequent SDT nodes shall have new identifiers assigned to them when the document is loaded.
* During standalone SDT [Clone()](../) operation new unique ID will be generated for the cloned SDT node.
* If Id is not specified in the source document, then the SDT node shall have a new unique identifier assigned to it when the document is loaded.



## Examples



Shows how to create a structured document tag in a plain text box and modify its appearance. 
```cpp
auto doc = MakeObject<Document>();

// Create a structured document tag that will contain plain text.
auto tag = MakeObject<StructuredDocumentTag>(doc, SdtType::PlainText, MarkupLevel::Inline);

// Set the title and color of the frame that appears when you mouse over the structured document tag in Microsoft Word.
tag->set_Title(u"My plain text");
tag->set_Color(System::Drawing::Color::get_Magenta());

// Set a tag for this structured document tag, which is obtainable
// as an XML element named "tag", with the string below in its "@val" attribute.
tag->set_Tag(u"MyPlainTextSDT");

// Every structured document tag has a random unique ID.
ASSERT_GT(tag->get_Id(), 0);

// Set the font for the text inside the structured document tag.
tag->get_ContentsFont()->set_Name(u"Arial");

// Set the font for the text at the end of the structured document tag.
// Any text that we type in the document body after moving out of the tag with arrow keys will use this font.
tag->get_EndCharacterFont()->set_Name(u"Arial Black");

// By default, this is false and pressing enter while inside a structured document tag does nothing.
// When set to true, our structured document tag can have multiple lines.

// Set the "Multiline" property to "false" to only allow the contents
// of this structured document tag to span a single line.
// Set the "Multiline" property to "true" to allow the tag to contain multiple lines of content.
tag->set_Multiline(true);

// Set the "Appearance" property to "SdtAppearance.Tags" to show tags around content.
// By default structured document tag shows as BoundingBox.
tag->set_Appearance(SdtAppearance::Tags);

auto builder = MakeObject<DocumentBuilder>(doc);
builder->InsertNode(tag);

// Insert a clone of our structured document tag in a new paragraph.
auto tagClone = System::DynamicCast<StructuredDocumentTag>(tag->Clone(true));
builder->InsertParagraph();
builder->InsertNode(tagClone);

// Use the "RemoveSelfOnly" method to remove a structured document tag, while keeping its contents in the document.
tagClone->RemoveSelfOnly();

doc->Save(ArtifactsDir + u"StructuredDocumentTag.PlainText.docx");
```

## See Also

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words](../../../)
