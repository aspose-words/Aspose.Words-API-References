---
title: "Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat Methode"
linktitle: "get_SaveFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat Methode. Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Save‑Options‑Objekt verwendet wird. Kann nur Xlsx in C++ sein."
type: docs
weight: 4000
url: /de/cpp/aspose.words.saving/xlsxsaveoptions/get_saveformat/
---
## XlsxSaveOptions::get_SaveFormat method


Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Save‑Options‑Objekt verwendet wird. Kann nur [Xlsx](../../../aspose.words/saveformat/) sein.

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat() override
```


## Beispiele



Zeigt, wie man ein XLSX-Dokument komprimiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape with linked chart.docx");

auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);
xlsxSaveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Xlsx);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
