---
title: "enumeración Aspose::Words::BorderType"
linktitle: "BorderType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "enumeración Aspose::Words::BorderType. Especifica los lados de un borde. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 81000
url: /es/cpp/aspose.words/bordertype/
---
## BorderType enum


Especifica los lados de un borde. Para obtener más información, visite el artículo de documentación [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
enum class BorderType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | -1 | Valor predeterminado. |
| Inferior | 0 | Especifica el borde inferior de un párrafo o una celda de tabla. |
| Izquierda | 1 | Especifica el borde izquierdo de un párrafo o una celda de tabla. |
| Derecha | 2 | Especifica el borde derecho de un párrafo o una celda de tabla. |
| Superior | 3 | Especifica el borde superior de un párrafo o una celda de tabla. |
| Horizontal | 4 | Especifica el borde horizontal entre celdas en una tabla o entre párrafos compatibles. |
| Vertical | 5 | Especifica el borde vertical entre celdas en una tabla. |
| DiagonalDown | 6 | Especifica el borde diagonal en una celda de tabla. |
| DiagonalUp | 7 | Especifica el borde diagonal en una celda de tabla. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
