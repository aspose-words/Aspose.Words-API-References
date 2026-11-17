---
title: Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding method
linktitle: get_Encoding
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding method. Specifies the encoding to use when exporting in text formats. Default value is Encoding.UTF8 in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.saving/txtsaveoptionsbase/get_encoding/
---
## TxtSaveOptionsBase::get_Encoding method


Specifies the encoding to use when exporting in text formats. Default value is **Encoding.UTF8**.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding() const
```


## Examples



Shows how to set encoding for a .txt output document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Add some text with characters from outside the ASCII character set.
builder->Write(u"À È Ì Ò Ù.");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Verify that the "Encoding" property contains the appropriate encoding for our document's contents.
ASPOSE_ASSERT_EQ(System::Text::Encoding::get_UTF8(), txtSaveOptions->get_Encoding());

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.Encoding.UTF8.txt", txtSaveOptions);

System::String docText = System::Text::Encoding::get_UTF8()->GetString(System::IO::File::ReadAllBytes(get_ArtifactsDir() + u"TxtSaveOptions.Encoding.UTF8.txt"));

ASSERT_EQ(u"\ufeffÀ È Ì Ò Ù.\r\n", docText);

// Using an unsuitable encoding may result in a loss of document contents.
txtSaveOptions->set_Encoding(System::Text::Encoding::get_ASCII());
doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.Encoding.ASCII.txt", txtSaveOptions);
docText = System::Text::Encoding::get_ASCII()->GetString(System::IO::File::ReadAllBytes(get_ArtifactsDir() + u"TxtSaveOptions.Encoding.ASCII.txt"));

ASSERT_EQ(u"? ? ? ? ?.\r\n", docText);
```

## See Also

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
