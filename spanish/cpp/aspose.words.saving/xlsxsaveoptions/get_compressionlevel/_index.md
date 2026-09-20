---
title: "Método Aspose::Words::Saving::XlsxSaveOptions::get_CompressionLevel"
linktitle: "get_CompressionLevel"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::XlsxSaveOptions::get_CompressionLevel. Especifica el nivel de compresión utilizado para guardar el documento. El valor predeterminado es Normal en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.saving/xlsxsaveoptions/get_compressionlevel/
---
## XlsxSaveOptions::get_CompressionLevel method


Especifica el nivel de compresión utilizado para guardar el documento. El valor predeterminado es [Normal](../../compressionlevel/).

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::XlsxSaveOptions::get_CompressionLevel() const
```


## Ejemplos



Muestra cómo comprimir un documento XLSX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape with linked chart.docx");

auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);
xlsxSaveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Xlsx);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

## Ver también

* Enum [CompressionLevel](../../compressionlevel/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
