---
title: Aspose::Words::Markup::StructuredDocumentTag::get_LockContentControl method
linktitle: get_LockContentControl
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTag::get_LockContentControl method. When set to true, this property will prohibit a user from deleting this SDT in C++.'
type: docs
weight: 22000
url: /cpp/aspose.words.markup/structureddocumenttag/get_lockcontentcontrol/
---
## StructuredDocumentTag::get_LockContentControl method


When set to **true**, this property will prohibit a user from deleting this **SDT**.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_LockContentControl() override
```


## Examples



Shows how to apply editing restrictions to structured document tags. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a plain text structured document tag, which acts as a text box that prompts the user to fill it in.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Set the "LockContents" property to "true" to prohibit the user from editing this text box's contents.
tag->set_LockContents(true);
builder->Write(u"The contents of this structured document tag cannot be edited: ");
builder->InsertNode(tag);

tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Set the "LockContentControl" property to "true" to prohibit the user from
// deleting this structured document tag manually in Microsoft Word.
tag->set_LockContentControl(true);

builder->InsertParagraph();
builder->Write(u"This structured document tag cannot be deleted but its contents can be edited: ");
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Lock.docx");
```

## See Also

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
