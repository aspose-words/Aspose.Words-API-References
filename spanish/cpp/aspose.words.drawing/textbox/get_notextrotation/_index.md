---
title: "Aspose::Words::Drawing::TextBox::get_NoTextRotation método"
linktitle: "get_NoTextRotation"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::TextBox::get_NoTextRotation método. Obtiene o establece un valor booleano que indica si el texto del TextBox no debe rotarse cuando la forma se rota en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.drawing/textbox/get_notextrotation/
---
## TextBox::get_NoTextRotation method


Obtiene o establece un valor booleano que indica si el texto del [TextBox](../) no debe rotarse cuando la forma se rota.

```cpp
bool Aspose::Words::Drawing::TextBox::get_NoTextRotation()
```

## Observaciones


El valor predeterminado es **false**

## Ejemplos



Muestra cómo desactivar la rotación del texto cuando la forma se rota.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Ellipse, 20, 20);
shape->get_TextBox()->set_NoTextRotation(true);

doc->Save(get_ArtifactsDir() + u"Shape.NoTextRotation.docx");
```

## Ver también

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
