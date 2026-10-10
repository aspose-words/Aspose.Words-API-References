---
title: "Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName metod"
linktitle: "get_ExportGeneratorName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName metod. När true, får namnet och versionen av Aspose.Words att bäddas in i producerade filer. Standardvärdet är true i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.saving/saveoptions/get_exportgeneratorname/
---
## SaveOptions::get_ExportGeneratorName method


När **true** görs namn och version av Aspose.Words inbäddade i de skapade filerna. Standardvärdet är **true**.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName() const
```


## Exempel



Visar hur man inaktiverar att lägga till namn och version av Aspose.Words i producerade filer.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Använd https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ för att veta hur man kontrollerar resultatet.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_ExportGeneratorName(false);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
```

## Se även

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
