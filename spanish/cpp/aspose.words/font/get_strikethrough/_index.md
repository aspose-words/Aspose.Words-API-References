---
title: "Método Aspose::Words::Font::get_StrikeThrough"
linktitle: "get_StrikeThrough"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Font::get_StrikeThrough. Verdadero si la fuente está formateada como texto tachado en C++."
type: docs
weight: 41000
url: /es/cpp/aspose.words/font/get_strikethrough/
---
## Font::get_StrikeThrough method


True si la fuente está formateada como texto tachado.

```cpp
bool Aspose::Words::Font::get_StrikeThrough()
```


## Ejemplos



Muestra cómo agregar una línea de tachado al texto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Text with a single-line strikethrough.");
run->get_Font()->set_StrikeThrough(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

para = System::ExplicitCast<Aspose::Words::Paragraph>(para->get_ParentNode()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));

run = System::MakeObject<Aspose::Words::Run>(doc, u"Text with a double-line strikethrough.");
run->get_Font()->set_DoubleStrikeThrough(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.StrikeThrough.docx");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
