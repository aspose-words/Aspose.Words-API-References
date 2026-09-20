---
title: "Método Aspose::Words::Font::get_Position"
linktitle: "get_Position"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Font::get_Position. Obtiene o establece la posición del texto (en puntos) respecto a la línea base. Un número positivo eleva el texto, y un número negativo lo baja en C++."
type: docs
weight: 32000
url: /es/cpp/aspose.words/font/get_position/
---
## Font::get_Position method


Obtiene o establece la posición del texto (en puntos) relativa a la línea base. Un número positivo eleva el texto, y un número negativo lo baja.

```cpp
double Aspose::Words::Font::get_Position()
```


## Ejemplos



Muestra cómo formatear texto para desplazar su posición.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Eleva este fragmento de texto 5 puntos por encima de la línea base.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Raised text. ");
run->get_Font()->set_Position(5);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Baja este fragmento de texto 10 puntos por debajo de la línea base.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Lowered text. ");
run->get_Font()->set_Position(-10);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Añade un fragmento de texto normal.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Text in its default position. ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Añade un fragmento de texto que aparece como subíndice.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Subscript. ");
run->get_Font()->set_Subscript(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Añade un fragmento de texto que aparece como superíndice.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Superscript.");
run->get_Font()->set_Superscript(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.PositionSubscript.docx");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
