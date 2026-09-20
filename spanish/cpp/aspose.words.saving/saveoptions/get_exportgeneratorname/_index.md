---
title: "Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName método"
linktitle: "get_ExportGeneratorName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName método. Cuando es verdadero, hace que el nombre y la versión de Aspose.Words se incrusten en los archivos generados. El valor predeterminado es verdadero en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.saving/saveoptions/get_exportgeneratorname/
---
## SaveOptions::get_ExportGeneratorName method


Cuando **true**, hace que el nombre y la versión de Aspose.Words se incrusten en los archivos generados. El valor predeterminado es **true**.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName() const
```


## Ejemplos



Muestra cómo desactivar la adición del nombre y la versión de Aspose.Words en los archivos generados.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Use https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ para saber cómo comprobar el resultado.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_ExportGeneratorName(false);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
```

## Ver también

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
