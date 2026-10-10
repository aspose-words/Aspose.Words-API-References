---
title: "Aspose::Words::Drawing::TextBox class"
linktitle: "Cuadro de texto"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::TextBox class. Define atributos que especifican cómo se muestra un texto dentro de una forma. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 15000
url: /es/cpp/aspose.words.drawing/textbox/
---
## TextBox class


Define atributos que especifican cómo se muestra un texto dentro de una forma. Para obtener más información, visite el artículo de documentación [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class TextBox : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [BreakForwardLink](./breakforwardlink/)() | Rompe el enlace al siguiente [TextBox](./). |
| [get_FitShapeToText](./get_fitshapetotext/)() | Determina si Microsoft Word ampliará la forma para ajustarse al texto. |
| [get_InternalMarginBottom](./get_internalmarginbottom/)() | Especifica el margen interior inferior en puntos para una forma. |
| [get_InternalMarginLeft](./get_internalmarginleft/)() | Especifica el margen interior izquierdo en puntos para una forma. |
| [get_InternalMarginRight](./get_internalmarginright/)() | Especifica el margen interior derecho en puntos para una forma. |
| [get_InternalMarginTop](./get_internalmargintop/)() | Especifica el margen interior superior en puntos para una forma. |
| [get_LayoutFlow](./get_layoutflow/)() | Determina el flujo del diseño del texto en una forma. |
| [get_Next](./get_next/)() | Devuelve o establece un [TextBox](./) que representa el siguiente [TextBox](./) en una secuencia de formas. |
| [get_NoTextRotation](./get_notextrotation/)() | Obtiene o establece un valor booleano que indica si el texto del [TextBox](./) no debe rotarse cuando la forma se gira. |
| [get_Parent](./get_parent/)() const | Obtiene una forma padre para el [TextBox](./). |
| [get_Previous](./get_previous/)() | Devuelve un [TextBox](./) que representa el [TextBox](./) anterior en una secuencia de formas. |
| [get_TextBoxWrapMode](./get_textboxwrapmode/)() | Determina cómo el texto se envuelve dentro de una forma. |
| [get_VerticalAnchor](./get_verticalanchor/)() | Especifica la alineación vertical del texto dentro de una forma. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsValidLinkTarget](./isvalidlinktarget/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\>\&) | Determina si este [TextBox](./) puede enlazarse al [TextBox](./) objetivo. |
| [set_FitShapeToText](./set_fitshapetotext/)(bool) | Establecedor para [Aspose::Words::Drawing::TextBox::get_FitShapeToText](./get_fitshapetotext/). |
| [set_InternalMarginBottom](./set_internalmarginbottom/)(double) | Establecedor para [Aspose::Words::Drawing::TextBox::get_InternalMarginBottom](./get_internalmarginbottom/). |
| [set_InternalMarginLeft](./set_internalmarginleft/)(double) | Establecedor para [Aspose::Words::Drawing::TextBox::get_InternalMarginLeft](./get_internalmarginleft/). |
| [set_InternalMarginRight](./set_internalmarginright/)(double) | Establecedor para [Aspose::Words::Drawing::TextBox::get_InternalMarginRight](./get_internalmarginright/). |
| [set_InternalMarginTop](./set_internalmargintop/)(double) | Establecedor para [Aspose::Words::Drawing::TextBox::get_InternalMarginTop](./get_internalmargintop/). |
| [set_LayoutFlow](./set_layoutflow/)(Aspose::Words::Drawing::LayoutFlow) | Establecedor para [Aspose::Words::Drawing::TextBox::get_LayoutFlow](./get_layoutflow/). |
| [set_Next](./set_next/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\>\&) | Establecedor para [Aspose::Words::Drawing::TextBox::get_Next](./get_next/). |
| [set_NoTextRotation](./set_notextrotation/)(bool) | Establecedor para [Aspose::Words::Drawing::TextBox::get_NoTextRotation](./get_notextrotation/). |
| [set_TextBoxWrapMode](./set_textboxwrapmode/)(Aspose::Words::Drawing::TextBoxWrapMode) | Establecedor para [Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode](./get_textboxwrapmode/). |
| [set_VerticalAnchor](./set_verticalanchor/)(Aspose::Words::Drawing::TextBoxAnchor) | Establecedor para [Aspose::Words::Drawing::TextBox::get_VerticalAnchor](./get_verticalanchor/). |
| static [Type](./type/)() |  |
## Observaciones


Utiliza la propiedad [TextBox](../shape/get_textbox/) para acceder a las propiedades de texto de una forma. No creas instancias de la clase [TextBox](./) directamente.

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


Muestra cómo establecer márgenes internos para un cuadro de texto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta otro cuadro de texto con márgenes específicos.
System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();
textBox->set_InternalMarginTop(15);
textBox->set_InternalMarginBottom(15);
textBox->set_InternalMarginLeft(15);
textBox->set_InternalMarginRight(15);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text placed according to textbox margins.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxMargins.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
