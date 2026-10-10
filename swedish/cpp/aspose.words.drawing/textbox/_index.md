---
title: "Aspose::Words::Drawing::TextBox class"
linktitle: "Textruta"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::TextBox class. Definierar attribut som anger hur text visas inuti en form. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 15000
url: /sv/cpp/aspose.words.drawing/textbox/
---
## TextBox class


Definierar attribut som anger hur text visas inuti en form. För att lära dig mer, besök dokumentationsartikeln [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class TextBox : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [BreakForwardLink](./breakforwardlink/)() | Bryter länken till nästa [TextBox](./). |
| [get_FitShapeToText](./get_fitshapetotext/)() | Bestämmer om Microsoft Word kommer att förstora formen för att passa texten. |
| [get_InternalMarginBottom](./get_internalmarginbottom/)() | Anger den inre nedre marginalen i punkter för en form. |
| [get_InternalMarginLeft](./get_internalmarginleft/)() | Anger den inre vänstra marginalen i punkter för en form. |
| [get_InternalMarginRight](./get_internalmarginright/)() | Anger den inre högra marginalen i punkter för en form. |
| [get_InternalMarginTop](./get_internalmargintop/)() | Anger den inre övre marginalen i punkter för en form. |
| [get_LayoutFlow](./get_layoutflow/)() | Bestämmer flödet för textlayouten i en form. |
| [get_Next](./get_next/)() | Returnerar eller anger en [TextBox](./) som representerar nästa [TextBox](./) i en sekvens av former. |
| [get_NoTextRotation](./get_notextrotation/)() | Hämtar eller anger ett booleskt värde som indikerar om texten i [TextBox](./) inte ska roteras när formen roteras. |
| [get_Parent](./get_parent/)() const | Hämtar en föräldraform för [TextBox](./). |
| [get_Previous](./get_previous/)() | Returnerar en [TextBox](./) som representerar föregående [TextBox](./) i en sekvens av former. |
| [get_TextBoxWrapMode](./get_textboxwrapmode/)() | Bestämmer hur texten radbryts inuti en form. |
| [get_VerticalAnchor](./get_verticalanchor/)() | Anger den vertikala justeringen av texten inom en form. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsValidLinkTarget](./isvalidlinktarget/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\>\&) | Bestämmer om denna [TextBox](./) kan länkas till mål-[TextBox](./). |
| [set_FitShapeToText](./set_fitshapetotext/)(bool) | Sättare för [Aspose::Words::Drawing::TextBox::get_FitShapeToText](./get_fitshapetotext/). |
| [set_InternalMarginBottom](./set_internalmarginbottom/)(double) | Sättare för [Aspose::Words::Drawing::TextBox::get_InternalMarginBottom](./get_internalmarginbottom/). |
| [set_InternalMarginLeft](./set_internalmarginleft/)(double) | Sättare för [Aspose::Words::Drawing::TextBox::get_InternalMarginLeft](./get_internalmarginleft/). |
| [set_InternalMarginRight](./set_internalmarginright/)(double) | Sättare för [Aspose::Words::Drawing::TextBox::get_InternalMarginRight](./get_internalmarginright/). |
| [set_InternalMarginTop](./set_internalmargintop/)(double) | Sättare för [Aspose::Words::Drawing::TextBox::get_InternalMarginTop](./get_internalmargintop/). |
| [set_LayoutFlow](./set_layoutflow/)(Aspose::Words::Drawing::LayoutFlow) | Sättare för [Aspose::Words::Drawing::TextBox::get_LayoutFlow](./get_layoutflow/). |
| [set_Next](./set_next/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\>\&) | Sättare för [Aspose::Words::Drawing::TextBox::get_Next](./get_next/). |
| [set_NoTextRotation](./set_notextrotation/)(bool) | Sättare för [Aspose::Words::Drawing::TextBox::get_NoTextRotation](./get_notextrotation/). |
| [set_TextBoxWrapMode](./set_textboxwrapmode/)(Aspose::Words::Drawing::TextBoxWrapMode) | Sättare för [Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode](./get_textboxwrapmode/). |
| [set_VerticalAnchor](./set_verticalanchor/)(Aspose::Words::Drawing::TextBoxAnchor) | Sättare för [Aspose::Words::Drawing::TextBox::get_VerticalAnchor](./get_verticalanchor/). |
| static [Type](./type/)() |  |
## Anmärkningar


Använd egenskapen [TextBox](../shape/get_textbox/) för att komma åt textegenskaperna för en form. Du skapar inte instanser av klassen [TextBox](./) direkt.

## Exempel



Visar hur man ställer in orienteringen av text i en textruta.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Flytta dokumentbyggaren in i TextBox och lägg till text.
builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Writeln(u"Hello world!");
builder->Write(u"Hello again!");

// Ställ in egenskapen "LayoutFlow" för att ange en orientering för textinnehållet i den här textrutan.
textBox->set_LayoutFlow(layoutFlow);

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxLayoutFlow.docx");
```


Visar hur man får en textruta att ändra storlek så att den passar innehållet tätt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Applicera dessa värden på båda dessa medlemmar för att få föräldraformen att passa
// tätt runt textinnehållet, utan att ta hänsyn till de dimensioner vi har angett.
textBox->set_FitShapeToText(true);
textBox->set_TextBoxWrapMode(Aspose::Words::Drawing::TextBoxWrapMode::None);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text fit tightly inside textbox.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxFitShapeToText.docx");
```


Visar hur man ställer in interna marginaler för en textruta.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en annan textruta med specifika marginaler.
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

## Se även

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
