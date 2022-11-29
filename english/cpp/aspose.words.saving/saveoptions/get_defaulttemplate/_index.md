---
title: get_DefaultTemplate
second_title: Aspose.Words for C++ API Reference
description: Gets or sets path to default template (including filename). Default value for this property is empty string.
type: docs
weight: 27
url: /cpp/aspose.words.saving/saveoptions/get_defaulttemplate/
---
## SaveOptions::get_DefaultTemplate method


Gets or sets path to default template (including filename). Default value for this property is **empty string**.

```cpp
System::String Aspose::Words::Saving::SaveOptions::get_DefaultTemplate() const
```


## Examples



Shows how to set a default template for documents that do not have attached templates. 
```cpp
auto doc = MakeObject<Document>();

// Enable automatic style updating, but do not attach a template document.
doc->set_AutomaticallyUpdateStyles(true);

ASSERT_EQ(String::Empty, doc->get_AttachedTemplate());

// Since there is no template document, the document had nowhere to track style changes.
// Use a SaveOptions object to automatically set a template
// if a document that we are saving does not have one.
SharedPtr<SaveOptions> options = SaveOptions::CreateSaveOptions(u"Document.DefaultTemplate.docx");
options->set_DefaultTemplate(MyDir + u"Business brochure.dotx");

doc->Save(ArtifactsDir + u"Document.DefaultTemplate.docx", options);
```

## See Also

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
