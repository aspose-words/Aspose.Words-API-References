---
title: Aspose::Words::Saving::DocSaveOptions::get_Password method
linktitle: get_Password
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::DocSaveOptions::get_Password method. Gets/sets a password to encrypt document using RC4 encryption method in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.saving/docsaveoptions/get_password/
---
## DocSaveOptions::get_Password method


Gets/sets a password to encrypt document using RC4 encryption method.

```cpp
System::String Aspose::Words::Saving::DocSaveOptions::get_Password() const
```

## Remarks


In order to save document without encryption this property should be **null** or empty string.

## Examples



Shows how to set save options for older Microsoft Word formats. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto options = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>(Aspose::Words::SaveFormat::Doc);

// Set a password which will protect the loading of the document by Microsoft Word or Aspose.Words.
// Note that this does not encrypt the contents of the document in any way.
options->set_Password(u"MyPassword");

// If the document contains a routing slip, we can preserve it while saving by setting this flag to true.
options->set_SaveRoutingSlip(true);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", options);

// To be able to load the document,
// we will need to apply the password we specified in the DocSaveOptions object in a LoadOptions object.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc");
})(), Aspose::Words::IncorrectPasswordException);

auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"MyPassword");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", loadOptions);

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## See Also

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
