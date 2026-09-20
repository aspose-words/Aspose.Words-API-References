---
title: "Aspose::Words::PageBorderDistanceFrom enumeración"
linktitle: "PageBorderDistanceFrom"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::PageBorderDistanceFrom enumeración. Especifica la posición del borde de página relativo al margen de la página en C++."
type: docs
weight: 107000
url: /es/cpp/aspose.words/pageborderdistancefrom/
---
## PageBorderDistanceFrom enum


Especifica la posición del borde de la página en relación con el margen de la página.

```cpp
enum class PageBorderDistanceFrom
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Text | 0 | La posición de [Border](../border/) se mide desde el margen de la página. |
| PageEdge | 1 | La posición de [Border](../border/) se mide desde el borde de la página. |


## Ejemplos



Muestra cómo crear un borde de banda azul ancha en la parte superior de la primera página.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_BorderAlwaysInFront(false);
pageSetup->set_BorderDistanceFrom(Aspose::Words::PageBorderDistanceFrom::PageEdge);
pageSetup->set_BorderAppliesTo(Aspose::Words::PageBorderAppliesTo::FirstPage);

System::SharedPtr<Aspose::Words::Border> border = pageSetup->get_Borders()->idx_get(Aspose::Words::BorderType::Top);
border->set_LineStyle(Aspose::Words::LineStyle::Single);
border->set_LineWidth(30);
border->set_Color(System::Drawing::Color::get_Blue());
border->set_DistanceFromText(0);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorderProperties.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
