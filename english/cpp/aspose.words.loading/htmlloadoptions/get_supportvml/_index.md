---
title: Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml method
linktitle: get_SupportVml
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml method. Gets or sets a value indicating whether to support VML images in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.loading/htmlloadoptions/get_supportvml/
---
## HtmlLoadOptions::get_SupportVml method


Gets or sets a value indicating whether to support VML images.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml() const
```


## Examples



Shows how to support conditional comments while loading an HTML document. 
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// If the value is true, then we take VML code into account while parsing the loaded document.
loadOptions->set_SupportVml(supportVml);

// This document contains a JPEG image within "<!--[if gte vml 1]>" tags,
// and a different PNG image within "<![if !vml]>" tags.
// If we set the "SupportVml" flag to "true", then Aspose.Words will load the JPEG.
// If we set this flag to "false", then Aspose.Words will only load the PNG.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## See Also

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
