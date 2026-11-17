---
title: Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding method
linktitle: get_Encoding
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding method. Specifies the encoding to use when exporting to HTML. Default value is new UTF8Encoding(true) (UTF-8 with BOM) in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.saving/htmlfixedsaveoptions/get_encoding/
---
## HtmlFixedSaveOptions::get_Encoding method


Specifies the encoding to use when exporting to HTML. Default value is **new UTF8Encoding(true)** (UTF-8 with BOM).

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding() const
```


## Examples



Shows how to set which encoding to use while exporting a document to HTML. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello World!");

// The default encoding is UTF-8. If we want to represent our document using a different encoding,
// we can use a SaveOptions object to set a specific encoding.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_Encoding(System::Text::Encoding::get_ASCII());

ASSERT_EQ(u"US-ASCII", htmlFixedSaveOptions->get_Encoding()->get_EncodingName());

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

## See Also

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
