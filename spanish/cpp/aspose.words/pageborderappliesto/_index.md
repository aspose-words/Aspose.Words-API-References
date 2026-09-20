---
title: "Aspose::Words::PageBorderAppliesTo enum"
linktitle: "PageBorderAppliesTo"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::PageBorderAppliesTo enum. Especifica en qué páginas se imprime el borde de página en C++."
type: docs
weight: 106000
url: /es/cpp/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enum


Especifica en qué páginas se imprime el borde de la página.

```cpp
enum class PageBorderAppliesTo
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| AllPages | 0 | El borde de página se muestra en todas las páginas de la sección. |
| FirstPage | 1 | El borde de página se muestra solo en la primera página de la sección. |
| OtherPages | 2 | El borde de página se muestra en todas las páginas excepto la primera página de la sección. |


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
