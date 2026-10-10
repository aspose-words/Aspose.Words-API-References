---
title: "Aspose::Words::Saving::XlsxSectionMode enum"
linktitle: "XlsxSectionMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::XlsxSectionMode enum. Specifica come le sezioni vengono gestite durante il salvataggio di un documento nel formato XLSX in C++."
type: docs
weight: 87000
url: /it/cpp/aspose.words.saving/xlsxsectionmode/
---
## XlsxSectionMode enum


Specifica come le sezioni vengono gestite quando si salva un documento in formato XLSX.

```cpp
enum class XlsxSectionMode
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| MultipleWorksheets | 0 | Specifica che un foglio di lavoro separato viene creato per ogni sezione di un documento. |
| SingleWorksheet | 1 | Specifica che tutte le sezioni di un documento sono salvate su un unico foglio di lavoro. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
