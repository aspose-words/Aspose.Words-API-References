---
title: get_MemoryOptimization
second_title: Aspose.Words for C++ API Reference
description: Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is false.
type: docs
weight: 105
url: /cpp/aspose.words.saving/saveoptions/get_memoryoptimization/
---
## SaveOptions.get_MemoryOptimization method


Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_MemoryOptimization() const
```


## Examples




Shows an option to optimize memory consumption when rendering large documents to PDF. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
SharedPtr<SaveOptions> saveOptions = SaveOptions::CreateSaveOptions(SaveFormat::Pdf);

// Set the "MemoryOptimization" property to "true" to lower the memory footprint of large documents' saving operations
// at the cost of increasing the duration of the operation.
// Set the "MemoryOptimization" property to "false" to save the document as a PDF normally.
saveOptions->set_MemoryOptimization(memoryOptimization);

doc->Save(ArtifactsDir + u"PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

