---
title: Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase method
linktitle: get_HyperlinkBase
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase method. Specifies the base string used for evaluating relative hyperlinks in this document in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words.properties/builtindocumentproperties/get_hyperlinkbase/
---
## BuiltInDocumentProperties::get_HyperlinkBase method


Specifies the base string used for evaluating relative hyperlinks in this document.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase()
```

## Remarks


Aspose.Words does not use this property.

## Examples



Shows how to store the base part of a hyperlink in the document's properties. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a relative hyperlink to a document in the local file system named "Document.docx".
// Clicking on the link in Microsoft Word will open the designated document, if it is available.
builder->InsertHyperlink(u"Relative hyperlink", u"Document.docx", false);

// This link is relative. If there is no "Document.docx" in the same folder
// as the document that contains this link, the link will be broken.
ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"Document.docx"));
doc->Save(get_ArtifactsDir() + u"DocumentProperties.HyperlinkBase.BrokenLink.docx");

// The document we are trying to link to is in a different directory to the one we are planning to save the document in.
// We could fix links like this by putting an absolute filename in each one.
// Alternatively, we could provide a base link that every hyperlink with a relative filename
// will prepend to its link when we click on it.
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();
properties->set_HyperlinkBase(get_MyDir());

ASSERT_TRUE(System::IO::File::Exists(properties->get_HyperlinkBase() + (System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(doc->get_Range()->get_Fields()->idx_get(0)))->get_Address()));

doc->Save(get_ArtifactsDir() + u"DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

## See Also

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
