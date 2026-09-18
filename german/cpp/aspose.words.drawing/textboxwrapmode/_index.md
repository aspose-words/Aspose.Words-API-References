---
title: "Aspose::Words::Drawing::TextBoxWrapMode enum"
linktitle: "TextBoxWrapMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::TextBoxWrapMode enum. Gibt an, wie Text innerhalb einer Form in C++ umwickelt wird."
type: docs
weight: 40000
url: /de/cpp/aspose.words.drawing/textboxwrapmode/
---
## TextBoxWrapMode enum


Gibt an, wie Text innerhalb einer Form umbrochen wird.

```cpp
enum class TextBoxWrapMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Square | 0 | Text wird innerhalb einer Form umwickelt. |
| Keine | 2 | Text wird nicht innerhalb einer Form umwickelt. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
