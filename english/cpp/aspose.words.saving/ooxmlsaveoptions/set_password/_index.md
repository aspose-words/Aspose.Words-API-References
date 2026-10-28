---
title: Aspose::Words::Saving::OoxmlSaveOptions::set_Password method
linktitle: set_Password
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::OoxmlSaveOptions::set_Password method. Gets/sets a password to encrypt document using ECMA376 Standard encryption algorithm in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words.saving/ooxmlsaveoptions/set_password/
---
## OoxmlSaveOptions::set_Password method


Gets/sets a password to encrypt document using ECMA376 Standard encryption algorithm.

```cpp
void Aspose::Words::Saving::OoxmlSaveOptions::set_Password(const System::String & value)
```

## Remarks


In order to save document without encryption this property should be **null** or empty string.
## Examples


Shows how to create a password encrypted Office Open XML document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx", saveOptions);

// We will not be able to open this document with Microsoft Word or
// Aspose.Words without providing the correct password.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(System::String(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx"));
})(), Aspose::Words::IncorrectPasswordException);

// Open the encrypted document by passing the correct password in a LoadOptions object.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"MyPassword"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```
## See Also

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
