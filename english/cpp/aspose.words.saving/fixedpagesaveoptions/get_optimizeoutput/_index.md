---
title: get_OptimizeOutput
second_title: Aspose.Words for C++ API Reference
description: 'Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to true. Default is false.'
type: docs
weight: 66
url: /cpp/aspose.words.saving/fixedpagesaveoptions/get_optimizeoutput/
---
## FixedPageSaveOptions::get_OptimizeOutput method


Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to true. Default is false.

```cpp
virtual bool Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput()
```


## Examples



Shows how to optimize document objects while saving to xps. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Unoptimized document.docx");

// Create an "XpsSaveOptions" object to pass to the document's "Save" method
// to modify how that method converts the document to .XPS.
auto saveOptions = MakeObject<XpsSaveOptions>();

// Set the "OptimizeOutput" property to "true" to take measures such as removing nested or empty canvases
// and concatenating adjacent runs with identical formatting to optimize the output document's content.
// This may affect the appearance of the document.
// Set the "OptimizeOutput" property to "false" to save the document normally.
saveOptions->set_OptimizeOutput(optimizeOutput);

doc->Save(ArtifactsDir + u"XpsSaveOptions.OptimizeOutput.xps", saveOptions);
```

## See Also

* Class [FixedPageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
