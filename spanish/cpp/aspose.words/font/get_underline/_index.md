---
title: "Aspose::Words::Font::get_Underline método"
linktitle: "get_Underline"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Font::get_Underline método. Obtiene o establece el tipo de subrayado aplicado a la fuente en C++."
type: docs
weight: 55000
url: /es/cpp/aspose.words/font/get_underline/
---
## Font::get_Underline method


Obtiene o establece el tipo de subrayado aplicado a la fuente.

```cpp
Aspose::Words::Underline Aspose::Words::Font::get_Underline()
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


Muestra cómo insertar un campo de hipervínculo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Inserta un hipervínculo y enfatízalo con formato personalizado.
// El hipervínculo será un fragmento de texto clicable que nos llevará a la ubicación especificada en la URL.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Ctrl + clic izquierdo en el enlace del texto en Microsoft Word nos llevará a la URL mediante una nueva ventana del navegador web.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```


Muestra cómo configurar el estilo y el color de un subrayado de texto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Underline(Aspose::Words::Underline::Dotted);
builder->get_Font()->set_UnderlineColor(System::Drawing::Color::get_Red());

builder->Writeln(u"Underlined text.");

doc->Save(get_ArtifactsDir() + u"Font.Underlines.docx");
```

## Ver también

* Enum [Underline](../../underline/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
