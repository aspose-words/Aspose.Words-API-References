---
title: "Metodo get_SectionMode di Aspose::Words::Saving::XlsxSaveOptions"
linktitle: "get_SectionMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode. Ottiene o imposta il modo in cui le sezioni vengono gestite durante il salvataggio del documento XLSX di output. Il valore predefinito è MultipleWorksheets in C++."
type: docs
weight: 4500
url: /it/cpp/aspose.words.saving/xlsxsaveoptions/get_sectionmode/
---
## XlsxSaveOptions::get_SectionMode method


Ottiene o imposta il modo in cui le sezioni vengono gestite durante il salvataggio del documento XLSX di output. Il valore predefinito è [MultipleWorksheets](../../xlsxsectionmode/).

```cpp
Aspose::Words::Saving::XlsxSectionMode Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode() const
```


## Esempi



Mostra come salvare il documento come fogli di lavoro separati.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

// Ogni sezione di un documento verrà creata come foglio di lavoro separato.
// Usa 'SingleWorksheet' per visualizzare l'intero documento su un unico foglio di lavoro.
auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_SectionMode(Aspose::Words::Saving::XlsxSectionMode::MultipleWorksheets);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
```

## Vedi anche

* Enum [XlsxSectionMode](../../xlsxsectionmode/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
