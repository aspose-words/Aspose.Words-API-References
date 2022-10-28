---
title: get_LockContents
second_title: Aspose.Words for C++ API Reference
description: When set to true, this property will prohibit a user from editing the contents of this SDT.
type: docs
weight: 274
url: /cpp/aspose.words.markup/structureddocumenttag/get_lockcontents/
---
## StructuredDocumentTag.get_LockContents method


When set to true, this property will prohibit a user from editing the contents of this **SDT**.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_LockContents() override
```


## Examples




Shows how to apply editing restrictions to structured document tags. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a plain text structured document tag, which acts as a text box that prompts the user to fill it in.
auto tag = MakeObject<StructuredDocumentTag>(doc, SdtType::PlainText, MarkupLevel::Inline);

// Set the "LockContents" property to "true" to prohibit the user from editing this text box's contents.
tag->set_LockContents(true);
builder->Write(u"The contents of this structured document tag cannot be edited: ");
builder->InsertNode(tag);

tag = MakeObject<StructuredDocumentTag>(doc, SdtType::PlainText, MarkupLevel::Inline);

// Set the "LockContentControl" property to "true" to prohibit the user from
// deleting this structured document tag manually in Microsoft Word.
tag->set_LockContentControl(true);

builder->InsertParagraph();
builder->Write(u"This structured document tag cannot be deleted but its contents can be edited: ");
builder->InsertNode(tag);

doc->Save(ArtifactsDir + u"StructuredDocumentTag.Lock.docx");
```

