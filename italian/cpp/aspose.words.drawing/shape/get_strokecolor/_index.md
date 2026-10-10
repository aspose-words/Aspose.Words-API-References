---
title: "Aspose::Words::Drawing::Shape::get_StrokeColor metodo"
linktitle: "get_StrokeColor"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Shape::get_StrokeColor metodo. Definisce il colore di un tratto in C++."
type: docs
weight: 21000
url: /it/cpp/aspose.words.drawing/shape/get_strokecolor/
---
## Shape::get_StrokeColor method


Definisce il colore di un tratto.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Shape::get_StrokeColor()
```

## Note


Questo è un collegamento rapido alla proprietà [Color](../../stroke/get_color/).

Il valore predefinito è **Black**.

## Esempi



Mostra come riempire una forma con un colore solido.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Scrivi del testo, quindi coprilo con una forma fluttuante.
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::CloudCallout, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 25, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 25, 250, 150, Aspose::Words::Drawing::WrapType::None);

// Usa la proprietà "StrokeColor" per impostare il colore del contorno della forma.
shape->set_StrokeColor(System::Drawing::Color::get_CadetBlue());

// Usa la proprietà "FillColor" per impostare il colore dell'area interna della forma.
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

// La proprietà "Opacity" determina quanto è trasparente il colore su una scala da 0 a 1,
// con 1 completamente opaco e 0 invisibile.
// Il riempimento della forma per impostazione predefinita è completamente opaco, quindi non possiamo vedere il testo su cui questa forma è sovrapposta.
ASPOSE_ASSERT_EQ(1.0, shape->get_Fill()->get_Opacity());

// Imposta l'opacità del colore di riempimento della forma a un valore più basso in modo da poter vedere il testo sottostante.
shape->get_Fill()->set_Opacity(0.3);

doc->Save(get_ArtifactsDir() + u"Shape.Fill.docx");
```

## Vedi anche

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
