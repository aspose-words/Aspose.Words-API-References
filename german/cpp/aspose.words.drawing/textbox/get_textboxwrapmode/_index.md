---
title: "Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode Methode"
linktitle: "get_TextBoxWrapMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode Methode. Bestimmt, wie Text innerhalb eines Shapes in C++ umbrochen wird."
type: docs
weight: 13000
url: /de/cpp/aspose.words.drawing/textbox/get_textboxwrapmode/
---
## TextBox::get_TextBoxWrapMode method


Bestimmt, wie Text innerhalb einer Form umbrochen wird.

```cpp
Aspose::Words::Drawing::TextBoxWrapMode Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode()
```

## Hinweise


Der Standardwert ist [Square](../../textboxwrapmode/).

## Beispiele



Zeigt, wie man einen Umbruchmodus für den Inhalt einer Textbox festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 300);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Setzen Sie die Eigenschaft "TextBoxWrapMode" auf "TextBoxWrapMode.None", um die Breite der Textbox zu erhöhen.
// Um Text aufzunehmen, sollte er groß genug sein.
// Setzen Sie die Eigenschaft "TextBoxWrapMode" auf "TextBoxWrapMode.Square", um
// Alle Texte im Textfeld umbrechen, wobei die Abmessungen erhalten bleiben.
textBox->set_TextBoxWrapMode(textBoxWrapMode);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->get_Font()->set_Size(32);
builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxContentsWrapMode.docx");
```

## Siehe auch

* Enum [TextBoxWrapMode](../../textboxwrapmode/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
