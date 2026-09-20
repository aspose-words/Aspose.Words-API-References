---
title: "Método Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat"
linktitle: "get_SaveFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat. Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Sólo puede ser Xlsx en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.saving/xlsxsaveoptions/get_saveformat/
---
## XlsxSaveOptions::get_SaveFormat method


Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Sólo puede ser [Xlsx](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat() override
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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
