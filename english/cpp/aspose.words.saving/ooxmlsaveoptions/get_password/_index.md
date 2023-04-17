---
title: Aspose::Words::Saving::OoxmlSaveOptions::get_Password method
linktitle: get_Password
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::OoxmlSaveOptions::get_Password method. Gets/sets a password to encrypt document using ECMA376 Standard encryption algorithm in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.saving/ooxmlsaveoptions/get_password/
---
## OoxmlSaveOptions::get_Password method


Gets/sets a password to encrypt document using ECMA376 Standard encryption algorithm.

```cpp
System::String Aspose::Words::Saving::OoxmlSaveOptions::get_Password() const
```

## Remarks


In order to save document without encryption this property should be **null** or empty string.

## Examples



Shows how to create a password encrypted Office Open XML document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

auto saveOptions = MakeObject<OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(ArtifactsDir + u"OoxmlSaveOptions.Password.docx", saveOptions);

// We will not be able to open this document with Microsoft Word or
// Aspose.Words without providing the correct password.
ASSERT_THROW(doc = MakeObject<Document>(ArtifactsDir + u"OoxmlSaveOptions.Password.docx"), IncorrectPasswordException);

// Open the encrypted document by passing the correct password in a LoadOptions object.
doc = MakeObject<Document>(ArtifactsDir + u"OoxmlSaveOptions.Password.docx", MakeObject<LoadOptions>(u"MyPassword"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## See Also

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
