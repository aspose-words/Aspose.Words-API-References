---
title: "Aspose::Words::Drawing::TextBox::get_LayoutFlow método"
linktitle: "get_LayoutFlow"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::TextBox::get_LayoutFlow método. Determina el flujo del diseño de texto en una forma en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.drawing/textbox/get_layoutflow/
---
## TextBox::get_LayoutFlow method


Determina el flujo del diseño del texto en una forma.

```cpp
Aspose::Words::Drawing::LayoutFlow Aspose::Words::Drawing::TextBox::get_LayoutFlow()
```

## Observaciones


El valor predeterminado es [Horizontal](../../layoutflow/).

## Ejemplos



Muestra cómo establecer la orientación del texto dentro de un cuadro de texto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Mueve el generador de documentos al interior del TextBox y agrega texto.
builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Writeln(u"Hello world!");
builder->Write(u"Hello again!");

// Establece la propiedad "LayoutFlow" para definir una orientación del contenido de texto de este cuadro de texto.
textBox->set_LayoutFlow(layoutFlow);

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxLayoutFlow.docx");
```

## Ver también

* Enum [LayoutFlow](../../layoutflow/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
