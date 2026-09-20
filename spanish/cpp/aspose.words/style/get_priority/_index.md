---
title: "Aspose::Words::Style::get_Priority método"
linktitle: "get_Priority"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Style::get_Priority método. Obtiene/establece el valor entero que representa la prioridad para ordenar los estilos en el panel de tareas de Estilos en C++."
type: docs
weight: 16334
url: /es/cpp/aspose.words/style/get_priority/
---
## Style::get_Priority method


Obtiene/establece el valor entero que representa la prioridad para ordenar los estilos en el panel de tareas de Estilos.

```cpp
int32_t Aspose::Words::Style::get_Priority() const
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
