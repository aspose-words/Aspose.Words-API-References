---
title: Aspose::Words::Loading::LoadOptions::set_Encoding method
linktitle: set_Encoding
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::LoadOptions::set_Encoding method. Sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be null. Default is null in C++.'
type: docs
weight: 24000
url: /cpp/aspose.words.loading/loadoptions/set_encoding/
---
## LoadOptions::set_Encoding method


Sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be **null**. Default is **null**.

```cpp
void Aspose::Words::Loading::LoadOptions::set_Encoding(const System::SharedPtr<System::Text::Encoding> & value)
```

## Remarks


This property is used only when loading HTML, TXT, or CHM documents.

If encoding is not specified inside the document and this property is **null**, then the system will try to automatically detect the encoding.
## Examples


Shows how to set the encoding with which to open a document.

```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_Encoding(System::Text::Encoding::get_ASCII());

// Load the document while passing the LoadOptions object, then verify the document's contents.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_TRUE(doc->ToString(SaveFormat::Text).Contains(u"This is a sample text in English."));
```
## See Also

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
