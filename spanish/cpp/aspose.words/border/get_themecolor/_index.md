---
title: "Método Aspose::Words::Border::get_ThemeColor"
linktitle: "get_ThemeColor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Border::get_ThemeColor. Obtiene o establece el color de tema en el esquema de colores aplicado que está asociado con este objeto Border en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words/border/get_themecolor/
---
## Border::get_ThemeColor method


Obtiene o establece el color de tema en el esquema de colores aplicado que está asociado con este objeto [Border](../).

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Border::get_ThemeColor()
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

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
