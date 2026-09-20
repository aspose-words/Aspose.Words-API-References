---
title: "Aspose::Words::Saving::TxtOfficeMathExportMode enum"
linktitle: "TxtOfficeMathExportMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::TxtOfficeMathExportMode enum. Especifica cómo Aspose.Words exporta OfficeMath a Texto en C++."
type: docs
weight: 86250
url: /es/cpp/aspose.words.saving/txtofficemathexportmode/
---
## TxtOfficeMathExportMode enum


Especifica cómo Aspose.Words exporta OfficeMath a [Texto](../../aspose.words/saveformat/).

```cpp
enum class TxtOfficeMathExportMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Text | 0 | Exporta OfficeMath como texto plano. |
| Latex | 3 | Exporta OfficeMath como LaTeX. |


## Ejemplos



Muestra cómo exportar el objeto OfficeMath como LaTeX en TXT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::TxtOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```

## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
