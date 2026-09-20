---
title: "Aspose::Words::Drawing::LayoutFlow enum"
linktitle: "LayoutFlow"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::LayoutFlow enum. Determina el flujo del diseño de texto en un cuadro de texto en C++."
type: docs
weight: 30000
url: /es/cpp/aspose.words.drawing/layoutflow/
---
## LayoutFlow enum


Determina el flujo del diseño de texto en un cuadro de texto.

```cpp
enum class LayoutFlow
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Horizontal | 0 | El texto se muestra horizontalmente. |
| TopToBottomIdeographic | 1 | El texto ideográfico se muestra verticalmente. |
| BottomToTop | 2 | El texto se muestra verticalmente. |
| TopToBottom | 3 | El texto se muestra verticalmente. |
| HorizontalIdeographic | 4 | El texto ideográfico se muestra horizontalmente. |
| Vertical | 5 | El texto se muestra verticalmente. |


## Ejemplos



Muestra cómo agregar texto a un cuadro de texto y cambiar su orientación
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto textbox = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
textbox->set_Width(100);
textbox->set_Height(100);
textbox->get_TextBox()->set_LayoutFlow(Aspose::Words::Drawing::LayoutFlow::BottomToTop);

textbox->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc));
builder->InsertNode(textbox);

builder->MoveTo(textbox->get_FirstParagraph());
builder->Write(u"This text is flipped 90 degrees to the left.");

doc->Save(get_ArtifactsDir() + u"Drawing.TextBox.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
