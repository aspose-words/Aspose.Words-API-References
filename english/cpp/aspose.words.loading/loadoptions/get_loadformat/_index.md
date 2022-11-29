---
title: get_LoadFormat
second_title: Aspose.Words for C++ API Reference
description: Specifies the format of the document to be loaded. Default is Auto.
type: docs
weight: 92
url: /cpp/aspose.words.loading/loadoptions/get_loadformat/
---
## LoadOptions::get_LoadFormat method


Specifies the format of the document to be loaded. Default is [Auto](../../../aspose.words/loadformat/).

```cpp
Aspose::Words::LoadFormat Aspose::Words::Loading::LoadOptions::get_LoadFormat() const
```

## Remarks


It is recommended that you specify the [Auto](../../../aspose.words/loadformat/) value and let Aspose.Words detect the file format automatically. If you know the format of the document you are about to load, you can specify the format explicitly and this will slightly reduce the loading time by the overhead associated with auto detecting the format. If you specify an explicit load format and it will turn out to be wrong, the auto detection will be invoked and a second attempt to load the file will be made.

## Examples



Shows how to specify a base URI when opening an html document. 
```cpp
// Suppose we want to load an .html document that contains an image linked by a relative URI
// while the image is in a different location. In that case, we will need to resolve the relative URI into an absolute one.
// We can provide a base URI using an HtmlLoadOptions object.
auto loadOptions = MakeObject<HtmlLoadOptions>(LoadFormat::Html, u"", ImageDir);

ASSERT_EQ(LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = MakeObject<Document>(MyDir + u"Missing image.html", loadOptions);

// While the image was broken in the input .html, our custom base URI helped us repair the link.
auto imageShape = System::DynamicCast<Shape>(doc->GetChildNodes(NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// This output document will display the image that was missing.
doc->Save(ArtifactsDir + u"HtmlLoadOptions.BaseUri.docx");
```

## See Also

* Enum [LoadFormat](../../../aspose.words/loadformat/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words](../../../)
