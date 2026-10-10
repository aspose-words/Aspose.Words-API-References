---
title: "Aspose::Words::Drawing::TextBox::get_NoTextRotation Methode"
linktitle: "get_NoTextRotation"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::TextBox::get_NoTextRotation Methode. Gibt einen booleschen Wert zurück oder setzt ihn, der angibt, ob der Text der TextBox nicht rotiert werden soll, wenn die Form in C++ rotiert wird."
type: docs
weight: 10000
url: /de/cpp/aspose.words.drawing/textbox/get_notextrotation/
---
## TextBox::get_NoTextRotation method


Gibt einen booleschen Wert zurück oder setzt ihn, der angibt, ob der Text der [TextBox](../) nicht rotiert werden soll, wenn die Form rotiert wird.

```cpp
bool Aspose::Words::Drawing::TextBox::get_NoTextRotation()
```

## Hinweise


Der Standardwert ist **false**

## Beispiele



Zeigt, wie man die Textrotation deaktiviert, wenn die Form rotiert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Ellipse, 20, 20);
shape->get_TextBox()->set_NoTextRotation(true);

doc->Save(get_ArtifactsDir() + u"Shape.NoTextRotation.docx");
```

## Siehe auch

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
