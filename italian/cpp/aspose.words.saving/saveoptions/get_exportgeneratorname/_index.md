---
title: "Metodo Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName"
linktitle: "get_ExportGeneratorName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName. Quando è true, inserisce il nome e la versione di Aspose.Words nei file prodotti. Il valore predefinito è true in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.saving/saveoptions/get_exportgeneratorname/
---
## SaveOptions::get_ExportGeneratorName method


Quando **true**, fa sì che il nome e la versione di Aspose.Words vengano incorporati nei file prodotti. Il valore predefinito è **true**.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName() const
```


## Esempi



Mostra come disabilitare l'aggiunta del nome e della versione di Aspose.Words nei file prodotti.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Usa https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ per sapere come verificare il risultato.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_ExportGeneratorName(false);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
```

## Vedi anche

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
