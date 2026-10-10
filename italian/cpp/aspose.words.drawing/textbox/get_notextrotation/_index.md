---
title: "Aspose::Words::Drawing::TextBox::get_NoTextRotation metodo"
linktitle: "get_NoTextRotation"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::TextBox::get_NoTextRotation metodo. Ottiene o imposta un valore booleano che indica se il testo del TextBox non deve ruotare quando la forma è ruotata in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.drawing/textbox/get_notextrotation/
---
## TextBox::get_NoTextRotation method


Ottiene o imposta un valore booleano che indica se il testo del [TextBox](../) non deve ruotare quando la forma è ruotata.

```cpp
bool Aspose::Words::Drawing::TextBox::get_NoTextRotation()
```

## Note


Il valore predefinito è **false**

## Esempi



Mostra come disabilitare la rotazione del testo quando la forma è ruotata.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Ellipse, 20, 20);
shape->get_TextBox()->set_NoTextRotation(true);

doc->Save(get_ArtifactsDir() + u"Shape.NoTextRotation.docx");
```

## Vedi anche

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
