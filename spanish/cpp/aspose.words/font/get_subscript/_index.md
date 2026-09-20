---
title: "Método Aspose::Words::Font::get_Subscript"
linktitle: "get_Subscript"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Font::get_Subscript. Verdadero si la fuente está formateada como subíndice en C++."
type: docs
weight: 45000
url: /es/cpp/aspose.words/font/get_subscript/
---
## Font::get_Subscript method


True si la fuente está formateada como subíndice.

```cpp
bool Aspose::Words::Font::get_Subscript()
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
