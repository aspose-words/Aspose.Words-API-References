---
title: "Método Aspose::Words::PageSetup::get_BorderDistanceFrom"
linktitle: "get_BorderDistanceFrom"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::PageSetup::get_BorderDistanceFrom. Obtiene o establece un valor que indica si el borde de página especificado se mide desde el borde de la página o desde el texto que lo rodea en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/pagesetup/get_borderdistancefrom/
---
## PageSetup::get_BorderDistanceFrom method


Obtiene o establece un valor que indica si el borde de página especificado se mide desde el borde de la página o desde el texto que lo rodea.

```cpp
Aspose::Words::PageBorderDistanceFrom Aspose::Words::PageSetup::get_BorderDistanceFrom()
```


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

* Enum [PageBorderDistanceFrom](../../pageborderdistancefrom/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
