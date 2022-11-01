---
title: get_HyperlinkBase
second_title: Aspose.Words for C++ API Reference
description: Specifies the base string used for evaluating relative hyperlinks in this document.
type: docs
weight: 144
url: /cpp/aspose.words.properties/builtindocumentproperties/get_hyperlinkbase/
---
## BuiltInDocumentProperties.get_HyperlinkBase method


Specifies the base string used for evaluating relative hyperlinks in this document.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase()
```


Aspose.Words does not use this property.

## Examples




Shows how to store the base part of a hyperlink in the document's properties. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a relative hyperlink to a document in the local file system named "Document.docx".
// Clicking on the link in Microsoft Word will open the designated document, if it is available.
builder->InsertHyperlink(u"Relative hyperlink", u"Document.docx", false);

// This link is relative. If there is no "Document.docx" in the same folder
// as the document that contains this link, the link will be broken.
ASSERT_FALSE(System::IO::File::Exists(ArtifactsDir + u"Document.docx"));
doc->Save(ArtifactsDir + u"DocumentProperties.HyperlinkBase.BrokenLink.docx");

// The document we are trying to link to is in a different directory to the one we are planning to save the document in.
// We could fix links like this by putting an absolute filename in each one.
// Alternatively, we could provide a base link that every hyperlink with a relative filename
// will prepend to its link when we click on it.
SharedPtr<BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();
properties->set_HyperlinkBase(MyDir);

ASSERT_TRUE(System::IO::File::Exists(properties->get_HyperlinkBase() +
                                     (System::DynamicCast<FieldHyperlink>(doc->get_Range()->get_Fields()->idx_get(0)))->get_Address()));

doc->Save(ArtifactsDir + u"DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

