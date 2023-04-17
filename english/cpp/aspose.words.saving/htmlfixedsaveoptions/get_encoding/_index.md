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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Hello World!");

// The default encoding is UTF-8. If we want to represent our document using a different encoding,
// we can use a SaveOptions object to set a specific encoding.
auto htmlFixedSaveOptions = MakeObject<HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_Encoding(System::Text::Encoding::GetEncoding(u"ASCII"));

ASSERT_EQ(u"US-ASCII", htmlFixedSaveOptions->get_Encoding()->get_EncodingName());

doc->Save(ArtifactsDir + u"HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

## See Also

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
