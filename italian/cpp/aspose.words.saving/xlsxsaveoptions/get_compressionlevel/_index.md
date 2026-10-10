---
title: "Metodo get_CompressionLevel di Aspose::Words::Saving::XlsxSaveOptions"
linktitle: "get_CompressionLevel"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo get_CompressionLevel di Aspose::Words::Saving::XlsxSaveOptions. Specifica il livello di compressione utilizzato per salvare il documento. Il valore predefinito è Normal in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.saving/xlsxsaveoptions/get_compressionlevel/
---
## XlsxSaveOptions::get_CompressionLevel method


Specifica il livello di compressione usato per salvare il documento. Il valore predefinito è [Normal](../../compressionlevel/).

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::XlsxSaveOptions::get_CompressionLevel() const
```


## Esempi



Mostra come comprimere un documento XLSX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape with linked chart.docx");

auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);
xlsxSaveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Xlsx);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

## Vedi anche

* Enum [CompressionLevel](../../compressionlevel/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
