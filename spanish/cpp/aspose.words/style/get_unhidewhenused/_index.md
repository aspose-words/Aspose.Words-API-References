---
title: "Método Aspose::Words::Style::get_UnhideWhenUsed"
linktitle: "get_UnhideWhenUsed"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Style::get_UnhideWhenUsed. Obtiene/establece si el estilo usado en el documento actual se muestra en la galería de Estilos y en el panel de tareas de Estilos. True cuando el estilo usado debe mostrarse en la galería de Estilos en C++."
type: docs
weight: 19500
url: /es/cpp/aspose.words/style/get_unhidewhenused/
---
## Style::get_UnhideWhenUsed method


Obtiene/establece si el estilo usado en el documento actual se muestra en la galería de Estilos y en el panel de tareas de Estilos. Verdadero cuando el estilo usado debe mostrarse en la galería de Estilos.

```cpp
bool Aspose::Words::Style::get_UnhideWhenUsed() const
```


## Ejemplos



Muestra cómo priorizar y ocultar un estilo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> styleTitle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Subtitle);

if (styleTitle->get_Priority() == 9)
{
    styleTitle->set_Priority(10);
}

if (!styleTitle->get_UnhideWhenUsed())
{
    styleTitle->set_UnhideWhenUsed(true);
}

if (styleTitle->get_SemiHidden())
{
    styleTitle->set_SemiHidden(true);
}

doc->Save(get_ArtifactsDir() + u"Styles.StylePriority.docx");
```

## Ver también

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
