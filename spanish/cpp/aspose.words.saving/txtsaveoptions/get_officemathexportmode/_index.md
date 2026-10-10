---
title: "Método Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode"
linktitle: "get_OfficeMathExportMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode. Especifica cómo se escribirá OfficeMath en el archivo de salida. El valor predeterminado es Text en C++."
type: docs
weight: 5500
url: /es/cpp/aspose.words.saving/txtsaveoptions/get_officemathexportmode/
---
## TxtSaveOptions::get_OfficeMathExportMode method


Especifica cómo se escribirá OfficeMath en el archivo de salida. El valor predeterminado es [Text](../../txtofficemathexportmode/).

```cpp
Aspose::Words::Saving::TxtOfficeMathExportMode Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode() const
```


## Ejemplos



Muestra cómo exportar el objeto OfficeMath como LaTeX en TXT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::TxtOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```

## Ver también

* Enum [TxtOfficeMathExportMode](../../txtofficemathexportmode/)
* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
