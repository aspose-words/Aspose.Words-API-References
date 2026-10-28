---
title: Aspose::Words::Saving::XlsxSaveOptions::set_SaveFormat method
linktitle: set_SaveFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::XlsxSaveOptions::set_SaveFormat method. Specifies the format in which the document will be saved if this save options object is used. Can only be Xlsx in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.saving/xlsxsaveoptions/set_saveformat/
---
## XlsxSaveOptions::set_SaveFormat method


Specifies the format in which the document will be saved if this save options object is used. Can only be [Xlsx](../../../aspose.words/saveformat/).

```cpp
void Aspose::Words::Saving::XlsxSaveOptions::set_SaveFormat(Aspose::Words::SaveFormat value) override
```

## Examples


Shows how to compress XLSX document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Shape with linked chart.docx"));

auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_CompressionLevel(CompressionLevel::Maximum);
xlsxSaveOptions->set_SaveFormat(SaveFormat::Xlsx);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```
## See Also

* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
