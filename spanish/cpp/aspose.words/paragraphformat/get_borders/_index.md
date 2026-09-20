---
title: "Aspose::Words::ParagraphFormat::get_Borders método"
linktitle: "get_Borders"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ParagraphFormat::get_Borders método. Obtiene la colección de bordes del párrafo en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words/paragraphformat/get_borders/
---
## ParagraphFormat::get_Borders method


Obtiene la colección de bordes del párrafo.

```cpp
System::SharedPtr<Aspose::Words::BorderCollection> Aspose::Words::ParagraphFormat::get_Borders()
```


## Ejemplos



Muestra cómo insertar un párrafo con un borde superior.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// Establezca ThemeColor solo cuando LineWidth o LineStyle se hayan establecido.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## Ver también

* Class [BorderCollection](../../bordercollection/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
