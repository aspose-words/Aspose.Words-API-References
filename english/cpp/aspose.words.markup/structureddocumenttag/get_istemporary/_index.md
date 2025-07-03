---
title: Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary method
linktitle: get_IsTemporary
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary method. Specifies whether this SDT shall be removed from the WordProcessingML document when its contents are modified in C++.'
type: docs
weight: 19000
url: /cpp/aspose.words.markup/structureddocumenttag/get_istemporary/
---
## StructuredDocumentTag::get_IsTemporary method


Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents are modified.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary() const
```


## Examples



Shows how to make single-use controls. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Insert a plain text structured document tag,
// which will act as a plain text form that the user may enter text into.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Set the "IsTemporary" property to "true" to make the structured document tag disappear and
// assimilate its contents into the document after the user edits it once in Microsoft Word.
// Set the "IsTemporary" property to "false" to allow the user to edit the contents
// of the structured document tag any number of times.
tag->set_IsTemporary(isTemporary);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Please enter text: ");
builder->InsertNode(tag);

// Insert another structured document tag in the form of a check box and set its default state to "checked".
tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Checkbox, Aspose::Words::Markup::MarkupLevel::Inline);
tag->set_Checked(true);

// Set the "IsTemporary" property to "true" to make the check box become a symbol
// once the user clicks on it in Microsoft Word.
// Set the "IsTemporary" property to "false" to allow the user to click on the check box any number of times.
tag->set_IsTemporary(isTemporary);

builder->Write(u"\nPlease click the check box: ");
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.IsTemporary.docx");
```

## See Also

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
