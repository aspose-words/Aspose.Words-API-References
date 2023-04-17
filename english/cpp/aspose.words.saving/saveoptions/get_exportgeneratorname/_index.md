---
title: Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName method
linktitle: get_ExportGeneratorName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName method. When true, causes the name and version of Aspose.Words to be embedded into produced files. Default value is true in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.saving/saveoptions/get_exportgeneratorname/
---
## SaveOptions::get_ExportGeneratorName method


When **true**, causes the name and version of Aspose.Words to be embedded into produced files. Default value is **true**.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName() const
```


## Examples



Shows how to disable adding name and version of Aspose.Words into produced files. 
```cpp
auto doc = MakeObject<Document>();

// Use https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ to know how to check the result.
auto saveOptions = MakeObject<OoxmlSaveOptions>();
saveOptions->set_ExportGeneratorName(false);

doc->Save(ArtifactsDir + u"OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
```

## See Also

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
