---
title: "enumeración Aspose::Words::Saving::XlsxSectionMode"
linktitle: "XlsxSectionMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "enumeración Aspose::Words::Saving::XlsxSectionMode. Especifica cómo se manejan las secciones al guardar un documento en formato XLSX en C++."
type: docs
weight: 87000
url: /es/cpp/aspose.words.saving/xlsxsectionmode/
---
## XlsxSectionMode enum


Especifica cómo se manejan las secciones al guardar un documento en formato XLSX.

```cpp
enum class XlsxSectionMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| MultipleWorksheets | 0 | Especifica que se crea una hoja de cálculo separada para cada sección de un documento. |
| SingleWorksheet | 1 | Especifica que todas las secciones de un documento se guardan en una sola hoja de cálculo. |


## Ejemplos



Muestra cómo guardar el documento como hojas de cálculo separadas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

// Cada sección de un documento se creará como una hoja de cálculo separada.
// Use 'SingleWorksheet' para mostrar todo el documento en una sola hoja de cálculo.
auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_SectionMode(Aspose::Words::Saving::XlsxSectionMode::MultipleWorksheets);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
```

## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
