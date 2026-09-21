---
title: "Aspose::Words::Drawing::TextBoxWrapMode enum"
linktitle: "TextBoxWrapMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::TextBoxWrapMode enum. Anger hur text omsluts inuti en form i C++."
type: docs
weight: 40000
url: /sv/cpp/aspose.words.drawing/textboxwrapmode/
---
## TextBoxWrapMode enum


Anger hur text omsluter inuti en form.

```cpp
enum class TextBoxWrapMode
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Square | 0 | Text omsluts inuti en form. |
| None | 2 | Text omsluts inte inuti en form. |


## Exempel



Visar hur man ställer in ett omslagläge för innehållet i en textruta.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 300);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Ställ in egenskapen "TextBoxWrapMode" till "TextBoxWrapMode.None" för att öka textrutans bredd
// för att rymma text, om den är tillräckligt stor.
// Ställ in egenskapen "TextBoxWrapMode" till "TextBoxWrapMode.Square" för att
// omsluta all text i textrutan och bevara dess dimensioner.
textBox->set_TextBoxWrapMode(textBoxWrapMode);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->get_Font()->set_Size(32);
builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxContentsWrapMode.docx");
```

## Se även

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
