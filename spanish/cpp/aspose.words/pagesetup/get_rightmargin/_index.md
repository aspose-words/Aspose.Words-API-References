---
title: "Aspose::Words::PageSetup::get_RightMargin método"
linktitle: "get_RightMargin"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::PageSetup::get_RightMargin método. Devuelve o establece la distancia (en puntos) entre el borde derecho de la página y el límite derecho del texto del cuerpo en C++."
type: docs
weight: 39000
url: /es/cpp/aspose.words/pagesetup/get_rightmargin/
---
## PageSetup::get_RightMargin method


Devuelve o establece la distancia (en puntos) entre el borde derecho de la página y el límite derecho del texto del cuerpo.

```cpp
double Aspose::Words::PageSetup::get_RightMargin()
```


## Ejemplos



Muestra cómo ajustar el tamaño del papel, la orientación, los márgenes, junto con otras configuraciones para una sección.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Legal);
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_HeaderDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));
builder->get_PageSetup()->set_FooterDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));

builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PageSetup.PageMargins.docx");
```

## Ver también

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
