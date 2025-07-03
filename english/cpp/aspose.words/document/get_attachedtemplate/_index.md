---
title: Aspose::Words::Document::get_AttachedTemplate method
linktitle: get_AttachedTemplate
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_AttachedTemplate method. Gets or sets the full path of the template attached to the document in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words/document/get_attachedtemplate/
---
## Document::get_AttachedTemplate method


Gets or sets the full path of the template attached to the document.

```cpp
System::String Aspose::Words::Document::get_AttachedTemplate()
```

## Remarks


Empty string means the document is attached to the Normal template.

## Examples



Shows how to set a default template for documents that do not have attached templates. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Enable automatic style updating, but do not attach a template document.
doc->set_AutomaticallyUpdateStyles(true);

ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// Since there is no template document, the document had nowhere to track style changes.
// Use a SaveOptions object to automatically set a template
// if a document that we are saving does not have one.
System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(u"Document.DefaultTemplate.docx");
options->set_DefaultTemplate(get_MyDir() + u"Business brochure.dotx");

doc->Save(get_ArtifactsDir() + u"Document.DefaultTemplate.docx", options);
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
