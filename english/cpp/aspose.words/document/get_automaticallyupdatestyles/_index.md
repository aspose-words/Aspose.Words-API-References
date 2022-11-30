---
title: get_AutomaticallyUpdateStyles
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word.
type: docs
weight: 157
url: /cpp/aspose.words/document/get_automaticallyupdatestyles/
---
## Document::get_AutomaticallyUpdateStyles method


Gets or sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word.

```cpp
bool Aspose::Words::Document::get_AutomaticallyUpdateStyles()
```


## Examples



Shows how to attach a template to a document. 
```cpp
auto doc = MakeObject<Document>();

// Microsoft Word documents by default come with an attached template called "Normal.dotm".
// There is no default template for blank Aspose.Words documents.
ASSERT_EQ(String::Empty, doc->get_AttachedTemplate());

// Attach a template, then set the flag to apply style changes
// within the template to styles in our document.
doc->set_AttachedTemplate(MyDir + u"Business brochure.dotx");
doc->set_AutomaticallyUpdateStyles(true);

doc->Save(ArtifactsDir + u"Document.AutomaticallyUpdateStyles.docx");
```


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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
