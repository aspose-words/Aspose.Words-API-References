---
title: "Aspose::Words::Drawing::ShapeBase::get_WrapType Methode"
linktitle: "get_WrapType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_WrapType-Methode. Definiert, ob die Form inline oder schwebend ist. Für schwebende Formen definiert sie den Umbruchmodus für Text um die Form in C++."
type: docs
weight: 56000
url: /de/cpp/aspose.words.drawing/shapebase/get_wraptype/
---
## ShapeBase::get_WrapType method


Definiert, ob die Form inline oder schwebend ist. Für schwebende Formen definiert es den Umbruchmodus für Text um die Form.

```cpp
Aspose::Words::Drawing::WrapType Aspose::Words::Drawing::ShapeBase::get_WrapType()
```

## Hinweise


Der Standardwert ist [None](../../wraptype/).

Wirkt nur bei Formen der obersten Ebene.

## Beispiele



Zeigt, wie man ein schwebendes Bild in die Mitte einer Seite einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie ein schwebendes Bild ein, das hinter dem überlappenden Text erscheint und es an der Seitenmitte ausrichtet.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```


Zeigt, wie man ein Textfeld erstellt und formatiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Erstelle ein schwebendes Textfeld.
auto textBox = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
textBox->set_WrapType(Aspose::Words::Drawing::WrapType::None);
textBox->set_Height(50);
textBox->set_Width(200);

// Lege die horizontale und vertikale Ausrichtung des Textes innerhalb der Form fest.
textBox->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
textBox->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Top);

// Füge dem Textfeld einen Absatz hinzu und füge einen Textlauf hinzu, den das Textfeld anzeigen soll.
textBox->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc));
System::SharedPtr<Aspose::Words::Paragraph> para = textBox->get_FirstParagraph();
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(textBox);

doc->Save(get_ArtifactsDir() + u"Shape.CreateTextBox.docx");
```

## Siehe auch

* Enum [WrapType](../../wraptype/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
