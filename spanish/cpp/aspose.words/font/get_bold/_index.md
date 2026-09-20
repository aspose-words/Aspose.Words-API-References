---
title: "Aspose::Words::Font::get_Bold método"
linktitle: "get_Bold"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Font::get_Bold método. Verdadero si la fuente está formateada en negrita en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/font/get_bold/
---
## Font::get_Bold method


Verdadero si la fuente está formateada en negrita.

```cpp
bool Aspose::Words::Font::get_Bold()
```


## Ejemplos



Muestra cómo insertar texto formateado usando [DocumentBuilder](../../documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Especifique el formato de fuente, luego agregue texto.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
