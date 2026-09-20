---
title: "Método Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode"
linktitle: "get_SectionMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode. Obtiene o establece la forma en que se manejan las secciones al guardar el documento XLSX de salida. El valor predeterminado es MultipleWorksheets en C++."
type: docs
weight: 4500
url: /es/cpp/aspose.words.saving/xlsxsaveoptions/get_sectionmode/
---
## XlsxSaveOptions::get_SectionMode method


Obtiene o establece la forma en que se manejan las secciones al guardar el documento XLSX de salida. El valor predeterminado es [MultipleWorksheets](../../xlsxsectionmode/).

```cpp
Aspose::Words::Saving::XlsxSectionMode Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode() const
```


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

* Enum [XlsxSectionMode](../../xlsxsectionmode/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
