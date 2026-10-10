---
title: "Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat method"
linktitle: "get_SaveFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat method. Anger det format i vilket dokumentet kommer att sparas om detta sparaalternativobjekt används. Kan endast vara Xlsx i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.saving/xlsxsaveoptions/get_saveformat/
---
## XlsxSaveOptions::get_SaveFormat method


Anger det format i vilket dokumentet kommer att sparas om detta sparaalternativobjekt används. Kan endast vara [Xlsx](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat() override
```


## Exempel



Visar hur man komprimerar XLSX-dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape with linked chart.docx");

auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);
xlsxSaveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Xlsx);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
