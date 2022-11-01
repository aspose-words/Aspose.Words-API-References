---
title: get_ExportGeneratorName
second_title: Aspose.Words for C++ API Reference
description: When true, causes the name and version of Aspose.Words to be embedded into produced files. Default value is true.
type: docs
weight: 79
url: /cpp/aspose.words.saving/saveoptions/get_exportgeneratorname/
---
## SaveOptions.get_ExportGeneratorName method


When true, causes the name and version of Aspose.Words to be embedded into produced files. Default value is **true**.

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

