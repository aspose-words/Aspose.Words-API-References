---
title: Aspose::Words::Markup::StructuredDocumentTag::RemoveSelfOnly method
linktitle: RemoveSelfOnly
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTag::RemoveSelfOnly method. Removes just this SDT node itself, but keeps the content of it inside the document tree in C++.'
type: docs
weight: 37000
url: /cpp/aspose.words.markup/structureddocumenttag/removeselfonly/
---
## StructuredDocumentTag::RemoveSelfOnly method


Removes just this SDT node itself, but keeps the content of it inside the document tree.

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::RemoveSelfOnly() override
```


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
auto tagClone = System::ExplicitCast<StructuredDocumentTag>(tag->Clone(true));
builder->InsertParagraph();
builder->InsertNode(tagClone);

// Use the "RemoveSelfOnly" method to remove a structured document tag, while keeping its contents in the document.
tagClone->RemoveSelfOnly();

doc->Save(ArtifactsDir + u"StructuredDocumentTag.PlainText.docx");
```

## See Also

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
