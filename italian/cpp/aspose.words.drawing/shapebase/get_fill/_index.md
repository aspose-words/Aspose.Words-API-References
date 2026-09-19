---
title: "Metodo Aspose::Words::Drawing::ShapeBase::get_Fill"
linktitle: "get_Fill"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::ShapeBase::get_Fill. Ottiene la formattazione di riempimento per la forma in C++."
type: docs
weight: 19000
url: /it/cpp/aspose.words.drawing/shapebase/get_fill/
---
## ShapeBase::get_Fill method


Ottiene la formattazione di riempimento per la forma.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Fill> Aspose::Words::Drawing::ShapeBase::get_Fill()
```


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

* Class [Fill](../../fill/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
