---
title: "Aspose::Words::Font::get_HighlightColor método"
linktitle: "get_HighlightColor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Font::get_HighlightColor método. Obtiene o establece el color de resaltado (marcador) en C++."
type: docs
weight: 17000
url: /es/cpp/aspose.words/font/get_highlightcolor/
---
## Font::get_HighlightColor method


Obtiene o establece el color de resaltado (marcador).

```cpp
System::Drawing::Color Aspose::Words::Font::get_HighlightColor()
```


## Ejemplos



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
