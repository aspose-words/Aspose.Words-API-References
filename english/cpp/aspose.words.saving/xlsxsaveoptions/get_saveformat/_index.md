---
title: Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat method
linktitle: get_SaveFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat method. Specifies the format in which the document will be saved if this save options object is used. Can only be Xlsx in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.saving/xlsxsaveoptions/get_saveformat/
---
## XlsxSaveOptions::get_SaveFormat method


Specifies the format in which the document will be saved if this save options object is used. Can only be [Xlsx](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat() override
```


## Examples



Shows how to compress XLSX document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape with linked chart.docx");

auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);
xlsxSaveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Xlsx);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
