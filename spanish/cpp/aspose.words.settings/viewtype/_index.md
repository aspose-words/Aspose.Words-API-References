---
title: "Aspose::Words::Settings::ViewType enumeración"
linktitle: "ViewType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Settings::ViewType enumeración. Valores posibles para el modo de vista en Microsoft Word en C++."
type: docs
weight: 21000
url: /es/cpp/aspose.words.settings/viewtype/
---
## ViewType enum


Valores posibles para el modo de vista en Microsoft Word.

```cpp
enum class ViewType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | El documento se mostrará en la vista predeterminada de la aplicación. |
| Lectura | 0 | El documento se mostrará en la vista predeterminada de la aplicación. |
| PageLayout | 1 | El documento se abrirá en una vista que muestra el documento tal como se imprimirá. |
| Outline | 3 | El documento se mostrará en una vista optimizada para esquematizar o crear documentos extensos. |
| Normal | 4 | El documento se mostrará en una vista optimizada para esquematizar o crear documentos extensos. |
| Web | 5 | El documento se mostrará en una vista que imita la forma en que este documento se mostraría en una página web. |


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
