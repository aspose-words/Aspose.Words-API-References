---
title: Aspose::Words::Saving::SaveOutputParameters::get_ContentType method
linktitle: get_ContentType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SaveOutputParameters::get_ContentType method. Returns the Content-Type string (Internet Media Type) that identifies the type of the saved document in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.saving/saveoutputparameters/get_contenttype/
---
## SaveOutputParameters::get_ContentType method


Returns the Content-Type string (Internet Media Type) that identifies the type of the saved document.

```cpp
System::String Aspose::Words::Saving::SaveOutputParameters::get_ContentType() const
```


## Examples



Shows how to access output parameters of a document's save operation. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// After we save a document, we can access the Internet Media Type (MIME type) of the newly created output document.
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.doc");

ASSERT_EQ(u"application/msword", parameters->get_ContentType());

// This property changes depending on the save format.
parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.pdf");

ASSERT_EQ(u"application/pdf", parameters->get_ContentType());
```

## See Also

* Class [SaveOutputParameters](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
