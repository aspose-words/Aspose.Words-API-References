---
title: "Méthode Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat"
linktitle: "get_SaveFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat. Spécifie le format dans lequel le document sera enregistré si cet objet d’options d’enregistrement est utilisé. Ne peut être que Xlsx en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/xlsxsaveoptions/get_saveformat/
---
## XlsxSaveOptions::get_SaveFormat method


Spécifie le format dans lequel le document sera enregistré si cet objet d’options d’enregistrement est utilisé. Ne peut être que [Xlsx](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat() override
```


## Exemples



Montre comment compresser un document XLSX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape with linked chart.docx");

auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);
xlsxSaveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Xlsx);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
