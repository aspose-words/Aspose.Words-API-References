---
title: "Aspose::Words::Font::get_Size método"
linktitle: "get_Size"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Font::get_Size método. Obtiene o establece el tamaño de la fuente en puntos en C++."
type: docs
weight: 36000
url: /es/cpp/aspose.words/font/get_size/
---
## Font::get_Size method


Obtiene o establece el tamaño de la fuente en puntos.

```cpp
double Aspose::Words::Font::get_Size()
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


Muestra cómo formatear una corrida de texto usando su propiedad de fuente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
