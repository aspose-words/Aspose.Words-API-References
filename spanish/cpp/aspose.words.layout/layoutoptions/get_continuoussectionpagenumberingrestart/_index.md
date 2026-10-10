---
title: "Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart método"
linktitle: "get_ContinuousSectionPageNumberingRestart"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart método. Obtiene o establece el modo de comportamiento para calcular los números de página cuando una sección continua reinicia la numeración de páginas en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.layout/layoutoptions/get_continuoussectionpagenumberingrestart/
---
## LayoutOptions::get_ContinuousSectionPageNumberingRestart method


Obtiene o establece el modo de comportamiento para calcular los números de página cuando una sección continua reinicia la numeración de páginas.

```cpp
Aspose::Words::Layout::ContinuousSectionRestart Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart() const
```


## Ejemplos



Muestra cómo controlar la numeración de páginas en una sección continua.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Continuous section page numbering.docx");

// Por defecto, el comportamiento de Aspose.Words coincide con Microsoft Word 2019.
// Si necesita el comportamiento antiguo de Aspose.Words, repetitivo de Microsoft Word 2016, use 'ContinuousSectionRestart.FromNewPageOnly'.
// La numeración de páginas se reinicia solo si no hay otro contenido antes de la sección en la página donde comienza la sección,
// por lo que la numeración se restablecerá a 2 a partir de la segunda página.
doc->get_LayoutOptions()->set_ContinuousSectionPageNumberingRestart(Aspose::Words::Layout::ContinuousSectionRestart::FromNewPageOnly);
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Layout.RestartPageNumberingInContinuousSection.pdf");
```

## Ver también

* Enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
