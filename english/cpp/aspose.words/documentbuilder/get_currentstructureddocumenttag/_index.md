---
title: Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag method
linktitle: get_CurrentStructuredDocumentTag
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag method. Gets the structured document tag that is currently selected in this DocumentBuilder in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words/documentbuilder/get_currentstructureddocumenttag/
---
## DocumentBuilder::get_CurrentStructuredDocumentTag method


Gets the structured document tag that is currently selected in this [DocumentBuilder](../).

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag()
```


## Examples



Shows how to move cursor of [DocumentBuilder](../) inside a structured document tag. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// There is a several ways to move the cursor:
// 1 -  Move to the first character of structured document tag by index.
builder->MoveToStructuredDocumentTag(1, 1);

// 2 -  Move to the first character of structured document tag by object.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 2, true));
builder->MoveToStructuredDocumentTag(tag, 1);
builder->Write(u" New text.");

ASSERT_EQ(u"R New text.ichText", tag->GetText().Trim());

// 3 -  Move to the end of the second structured document tag.
builder->MoveToStructuredDocumentTag(1, -1);
ASSERT_TRUE(builder->get_IsAtEndOfStructuredDocumentTag());

// Get currently selected structured document tag.
builder->get_CurrentStructuredDocumentTag()->set_Color(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Document.MoveToStructuredDocumentTag.docx");
```

## See Also

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
