---
title: "Aspose::Words::Drawing::TextBox::get_NoTextRotation metod"
linktitle: "get_NoTextRotation"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::TextBox::get_NoTextRotation metod. Hämtar eller anger ett booleskt värde som indikerar att texten i TextBoxen inte ska roteras när formen roteras i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.drawing/textbox/get_notextrotation/
---
## TextBox::get_NoTextRotation method


Hämtar eller anger ett booleskt värde som indikerar att texten i [TextBox](../) inte ska roteras när formen roteras.

```cpp
bool Aspose::Words::Drawing::TextBox::get_NoTextRotation()
```

## Anmärkningar


Standardvärdet är **false**

## Exempel



Visar hur man inaktiverar textrotation när formen roteras.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Ellipse, 20, 20);
shape->get_TextBox()->set_NoTextRotation(true);

doc->Save(get_ArtifactsDir() + u"Shape.NoTextRotation.docx");
```

## Se även

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
