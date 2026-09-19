---
title: "Aspose::Words::Saving::TxtOfficeMathExportMode enum"
linktitle: "TxtOfficeMathExportMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::TxtOfficeMathExportMode enum. Specifica come Aspose.Words esporta OfficeMath in testo in C++."
type: docs
weight: 86250
url: /it/cpp/aspose.words.saving/txtofficemathexportmode/
---
## TxtOfficeMathExportMode enum


Specifică come Aspose.Words esporta OfficeMath in [Text](../../aspose.words/saveformat/).

```cpp
enum class TxtOfficeMathExportMode
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Testo | 0 | Esporta OfficeMath come testo semplice. |
| Latex | 3 | Esporta OfficeMath come LaTeX. |


## Esempi



Mostra come esportare l'oggetto OfficeMath come Latex in TXT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::TxtOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
