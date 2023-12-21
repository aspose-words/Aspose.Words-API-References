---
title: Aspose::Words::Saving::HtmlFixedSaveOptions::get_OptimizeOutput method
linktitle: get_OptimizeOutput
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlFixedSaveOptions::get_OptimizeOutput method. Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formating are concatenated. Note: The accuracy of the content display may be affected if this property is set to true. Default is true in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.saving/htmlfixedsaveoptions/get_optimizeoutput/
---
## HtmlFixedSaveOptions::get_OptimizeOutput method


Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formating are concatenated. Note: The accuracy of the content display may be affected if this property is set to **true**. Default is **true**.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_OptimizeOutput() override
```


## Examples



Shows how to simplify a document when saving it to HTML by removing various redundant objects. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

auto saveOptions = MakeObject<HtmlFixedSaveOptions>();
saveOptions->set_OptimizeOutput(optimizeOutput);

doc->Save(ArtifactsDir + u"HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

// The size of the optimized version of the document is almost a third of the size of the unoptimized document.
ASSERT_NEAR(optimizeOutput ? 61836 : 191726,
            MakeObject<System::IO::FileInfo>(ArtifactsDir + u"HtmlFixedSaveOptions.OptimizeGraphicsOutput.html")->get_Length(), 200);
```

## See Also

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
