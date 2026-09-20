---
title: "Aspose::Words::Border::get_DistanceFromText método"
linktitle: "get_DistanceFromText"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Border::get_DistanceFromText método. Obtiene o establece la distancia del borde respecto al texto o al borde de la página en puntos en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words/border/get_distancefromtext/
---
## Border::get_DistanceFromText method


Obtiene o establece la distancia del borde al texto o al borde de la página en puntos.

```cpp
double Aspose::Words::Border::get_DistanceFromText()
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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
