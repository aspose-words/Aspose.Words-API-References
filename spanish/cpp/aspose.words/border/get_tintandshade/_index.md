---
title: "Aspose::Words::Border::get_TintAndShade método"
linktitle: "get_TintAndShade"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Border::get_TintAndShade método. Obtiene o establece un valor doble que aclara o oscurece un color en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words/border/get_tintandshade/
---
## Border::get_TintAndShade method


Obtiene o establece un valor doble que aclara u oscurece un color.

```cpp
double Aspose::Words::Border::get_TintAndShade()
```

## Observaciones


Los valores permitidos están en el rango de -1 (el más oscuro) a 1 (el más claro) para esta propiedad. Cero (0) es neutral.

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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
