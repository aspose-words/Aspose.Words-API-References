---
title: "Aspose::Words::Settings::ZoomType enum"
linktitle: "ZoomType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Settings::ZoomType enum. Valores posibles para el tamaño con el que el documento aparece en la pantalla en Microsoft Word en C++."
type: docs
weight: 22000
url: /es/cpp/aspose.words.settings/zoomtype/
---
## ZoomType enum


Valores posibles para el tamaño con el que el documento aparece en la pantalla en Microsoft Word.

```cpp
enum class ZoomType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Personalizado | 0 | El porcentaje de zoom se establece explícitamente. No se recalcula automáticamente cuando cambia el tamaño del control. |
| None | n/a | Indica que se use el porcentaje de zoom explícito. Igual que [Custom](./). |
| FullPage | 1 | El porcentaje de zoom se recalcula automáticamente para ajustarse a una página completa. |
| PageWidth | 2 | El porcentaje de zoom se recalcula automáticamente para ajustarse al ancho de la página. |
| TextFit | 3 | El porcentaje de zoom se recalcula automáticamente para ajustarse al texto. |


## Ejemplos



Muestra cómo establecer un factor de zoom personalizado, que las versiones anteriores de Microsoft Word aplicarán a un documento al cargarlo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->get_ViewOptions()->set_ViewType(Aspose::Words::Settings::ViewType::PageLayout);
doc->get_ViewOptions()->set_ZoomPercent(50);

ASSERT_EQ(Aspose::Words::Settings::ZoomType::Custom, doc->get_ViewOptions()->get_ZoomType());
ASSERT_EQ(Aspose::Words::Settings::ZoomType::None, doc->get_ViewOptions()->get_ZoomType());

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomPercentage.doc");
```

## Ver también

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
