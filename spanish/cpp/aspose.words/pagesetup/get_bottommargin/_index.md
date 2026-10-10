---
title: "Aspose::Words::PageSetup::get_BottomMargin método"
linktitle: "get_BottomMargin"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::PageSetup::get_BottomMargin método. Devuelve o establece la distancia (en puntos) entre el borde inferior de la página y el límite inferior del texto del cuerpo en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words/pagesetup/get_bottommargin/
---
## PageSetup::get_BottomMargin method


Devuelve o establece la distancia (en puntos) entre el borde inferior de la página y el límite inferior del texto del cuerpo.

```cpp
double Aspose::Words::PageSetup::get_BottomMargin()
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
