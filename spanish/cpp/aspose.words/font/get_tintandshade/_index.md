---
title: "Aspose::Words::Font::get_TintAndShade método"
linktitle: "get_TintAndShade"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Font::get_TintAndShade método. Obtiene o establece un valor doble que aclara o oscurece un color en C++."
type: docs
weight: 54000
url: /es/cpp/aspose.words/font/get_tintandshade/
---
## Font::get_TintAndShade method


Obtiene o establece un valor doble que aclara u oscurece un color.

```cpp
double Aspose::Words::Font::get_TintAndShade()
```

## Observaciones


Los valores permitidos están en el rango de -1 (más oscuro) a 1 (más claro) para esta propiedad.

Cero (0) es neutral.

## Ejemplos



Muestra cómo crear y usar un estilo con tema.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// Crea algún estilo con propiedades de fuente del tema.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"ThemedStyle");
style->get_Font()->set_ThemeFont(Aspose::Words::Themes::ThemeFont::Major);
style->get_Font()->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent5);
style->get_Font()->set_TintAndShade(0.3);

builder->get_ParagraphFormat()->set_StyleName(u"ThemedStyle");
builder->Writeln(u"Text with themed style");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
