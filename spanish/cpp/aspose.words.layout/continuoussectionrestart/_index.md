---
title: "Aspose::Words::Layout::ContinuousSectionRestart enum"
linktitle: "ContinuousSectionRestart"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Layout::ContinuousSectionRestart enum. Representa diferentes comportamientos al calcular los números de página en una sección continua que reinicia la numeración de páginas en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enum


Representa diferentes comportamientos al calcular los números de página en una sección continua que reinicia la numeración de páginas.

```cpp
enum class ContinuousSectionRestart
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Always | 0 | La numeración de páginas siempre se reinicia sin importar el flujo de contenido. |
| FromNewPageOnly | 1 | La numeración de páginas se reinicia solo si no hay otro contenido antes de la sección en la página donde comienza la sección. |


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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
