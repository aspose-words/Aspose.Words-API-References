---
title: "Metodo Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode"
linktitle: "get_OfficeMathExportMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode. Specifica come OfficeMath verrà scritto nel file di output. Il valore predefinito è Text in C++."
type: docs
weight: 5500
url: /it/cpp/aspose.words.saving/txtsaveoptions/get_officemathexportmode/
---
## TxtSaveOptions::get_OfficeMathExportMode method


Specifica come OfficeMath verrà scritto nel file di output. Il valore predefinito è [Text](../../txtofficemathexportmode/).

```cpp
Aspose::Words::Saving::TxtOfficeMathExportMode Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode() const
```


## Esempi



Mostra come esportare l'oggetto OfficeMath come Latex in TXT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::TxtOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```

## Vedi anche

* Enum [TxtOfficeMathExportMode](../../txtofficemathexportmode/)
* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
