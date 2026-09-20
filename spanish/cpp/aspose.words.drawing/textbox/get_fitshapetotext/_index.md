---
title: "Aspose::Words::Drawing::TextBox::get_FitShapeToText método"
linktitle: "get_FitShapeToText"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::TextBox::get_FitShapeToText método. Determina si Microsoft Word ampliará la forma para ajustarse al texto en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.drawing/textbox/get_fitshapetotext/
---
## TextBox::get_FitShapeToText method


Determina si Microsoft Word ampliará la forma para ajustarse al texto.

```cpp
bool Aspose::Words::Drawing::TextBox::get_FitShapeToText()
```

## Observaciones


El valor predeterminado es **false**.

## Ejemplos



Muestra cómo lograr que un cuadro de texto se redimensione automáticamente para ajustarse estrechamente a su contenido.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Aplica estos valores a ambos miembros para que la forma principal se ajuste
// estrechamente alrededor del contenido de texto, ignorando las dimensiones que hemos establecido.
textBox->set_FitShapeToText(true);
textBox->set_TextBoxWrapMode(Aspose::Words::Drawing::TextBoxWrapMode::None);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text fit tightly inside textbox.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxFitShapeToText.docx");
```

## Ver también

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
