---
title: "Aspose::Words::Style::get_SemiHidden método"
linktitle: "get_SemiHidden"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Style::get_SemiHidden método. Obtiene/establece si el estilo se oculta de la galería de Estilos y del panel de tareas de Estilos en C++."
type: docs
weight: 16667
url: /es/cpp/aspose.words/style/get_semihidden/
---
## Style::get_SemiHidden method


Obtiene/establece si el estilo se oculta de la galería de Estilos y del panel de tareas de Estilos.

```cpp
bool Aspose::Words::Style::get_SemiHidden() const
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
