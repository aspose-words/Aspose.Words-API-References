---
title: "Aspose::Words::Drawing::TextBox‑Klasse"
linktitle: "Textfeld"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::TextBox‑Klasse. Definiert Attribute, die festlegen, wie ein Text innerhalb einer Form angezeigt wird. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 15000
url: /de/cpp/aspose.words.drawing/textbox/
---
## TextBox class


Definiert Attribute, die festlegen, wie ein Text innerhalb einer Form angezeigt wird. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class TextBox : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [BreakForwardLink](./breakforwardlink/)() | Unterbricht die Verknüpfung zum nächsten [TextBox](./). |
| [get_FitShapeToText](./get_fitshapetotext/)() | Bestimmt, ob Microsoft Word die Form vergrößert, um den Text anzupassen. |
| [get_InternalMarginBottom](./get_internalmarginbottom/)() | Gibt den inneren unteren Rand in Punkten für eine Form an. |
| [get_InternalMarginLeft](./get_internalmarginleft/)() | Gibt den inneren linken Rand in Punkten für eine Form an. |
| [get_InternalMarginRight](./get_internalmarginright/)() | Gibt den inneren rechten Rand in Punkten für eine Form an. |
| [get_InternalMarginTop](./get_internalmargintop/)() | Gibt den inneren oberen Rand in Punkten für eine Form an. |
| [get_LayoutFlow](./get_layoutflow/)() | Bestimmt den Fluss des Textlayouts in einer Form. |
| [get_Next](./get_next/)() | Gibt ein [TextBox](./) zurück oder setzt es, das das nächste [TextBox](./) in einer Sequenz von Formen darstellt. |
| [get_NoTextRotation](./get_notextrotation/)() | Liest oder setzt einen booleschen Wert, der angibt, ob der Text des [TextBox](./) nicht rotiert werden soll, wenn die Form rotiert wird. |
| [get_Parent](./get_parent/)() const | Liefert die übergeordnete Form für das [TextBox](./). |
| [get_Previous](./get_previous/)() | Gibt ein [TextBox](./) zurück, das das vorherige [TextBox](./) in einer Sequenz von Formen darstellt. |
| [get_TextBoxWrapMode](./get_textboxwrapmode/)() | Bestimmt, wie Text innerhalb einer Form umbrochen wird. |
| [get_VerticalAnchor](./get_verticalanchor/)() | Gibt die vertikale Ausrichtung des Textes innerhalb einer Form an. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsValidLinkTarget](./isvalidlinktarget/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\>\&) | Bestimmt, ob dieses [TextBox](./) mit dem Ziel-[TextBox](./) verknüpft werden kann. |
| [set_FitShapeToText](./set_fitshapetotext/)(bool) | Setter für [Aspose::Words::Drawing::TextBox::get_FitShapeToText](./get_fitshapetotext/). |
| [set_InternalMarginBottom](./set_internalmarginbottom/)(double) | Setter für [Aspose::Words::Drawing::TextBox::get_InternalMarginBottom](./get_internalmarginbottom/). |
| [set_InternalMarginLeft](./set_internalmarginleft/)(double) | Setter für [Aspose::Words::Drawing::TextBox::get_InternalMarginLeft](./get_internalmarginleft/). |
| [set_InternalMarginRight](./set_internalmarginright/)(double) | Setter für [Aspose::Words::Drawing::TextBox::get_InternalMarginRight](./get_internalmarginright/). |
| [set_InternalMarginTop](./set_internalmargintop/)(double) | Setter für [Aspose::Words::Drawing::TextBox::get_InternalMarginTop](./get_internalmargintop/). |
| [set_LayoutFlow](./set_layoutflow/)(Aspose::Words::Drawing::LayoutFlow) | Setter für [Aspose::Words::Drawing::TextBox::get_LayoutFlow](./get_layoutflow/). |
| [set_Next](./set_next/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\>\&) | Setter für [Aspose::Words::Drawing::TextBox::get_Next](./get_next/). |
| [set_NoTextRotation](./set_notextrotation/)(bool) | Setter für [Aspose::Words::Drawing::TextBox::get_NoTextRotation](./get_notextrotation/). |
| [set_TextBoxWrapMode](./set_textboxwrapmode/)(Aspose::Words::Drawing::TextBoxWrapMode) | Setter für [Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode](./get_textboxwrapmode/). |
| [set_VerticalAnchor](./set_verticalanchor/)(Aspose::Words::Drawing::TextBoxAnchor) | Setter für [Aspose::Words::Drawing::TextBox::get_VerticalAnchor](./get_verticalanchor/). |
| static [Type](./type/)() |  |
## Hinweise


Verwenden Sie die [TextBox](../shape/get_textbox/) Eigenschaft, um auf Texteigenschaften einer Form zuzugreifen. Sie erstellen keine Instanzen der [TextBox](./) Klasse direkt.

## Beispiele



Zeigt, wie die Ausrichtung von Text innerhalb einer Textbox festgelegt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Bewegen Sie den Dokumenten-Builder in die TextBox und fügen Sie Text hinzu.
builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Writeln(u"Hello world!");
builder->Write(u"Hello again!");

// Setzen Sie die Eigenschaft "LayoutFlow", um eine Ausrichtung für den Textinhalt dieser Textbox festzulegen.
textBox->set_LayoutFlow(layoutFlow);

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxLayoutFlow.docx");
```


Zeigt, wie eine Textbox sich selbst so anpasst, dass sie ihren Inhalt eng umschließt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Wenden Sie diese Werte auf beide Mitglieder an, damit die übergeordnete Form passt
// eng um den Textinhalt herum, wobei die von uns festgelegten Abmessungen ignoriert werden.
textBox->set_FitShapeToText(true);
textBox->set_TextBoxWrapMode(Aspose::Words::Drawing::TextBoxWrapMode::None);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text fit tightly inside textbox.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxFitShapeToText.docx");
```


Zeigt, wie interne Ränder für eine Textbox festgelegt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie eine weitere Textbox mit bestimmten Rändern ein.
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

## Siehe auch

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
