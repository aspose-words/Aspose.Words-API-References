---
title: "Aspose::Words::Drawing::ShapeBase::get_DistanceRight method"
linktitle: "get_DistanceRight"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeBase::get_DistanceRight method. Restituisce o imposta la distanza (in punti) tra il testo del documento e il bordo destro della forma in C++."
type: docs
weight: 17000
url: /it/cpp/aspose.words.drawing/shapebase/get_distanceright/
---
## ShapeBase::get_DistanceRight method


Restituisce o imposta la distanza (in punti) tra il testo del documento e il bordo destro della forma.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_DistanceRight()
```

## Note


Il valore predefinito è 1/8 di pollice.

Ha effetto solo per le forme di livello superiore.

## Esempi



Mostra come impostare la distanza di avvolgimento per un testo che circonda una forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un rettangolo e fai avvolgere il testo strettamente attorno ai suoi bordi.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 150, 150);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Tight);

// Imposta la distanza minima tra la forma e il testo circostante a 40 pt su tutti i lati.
shape->set_DistanceTop(40);
shape->set_DistanceBottom(40);
shape->set_DistanceLeft(40);
shape->set_DistanceRight(40);

// Sposta la forma più vicino al centro della pagina, quindi ruota la forma di 60 gradi in senso orario.
shape->set_Top(75);
shape->set_Left(150);
shape->set_Rotation(60);

// Aggiungi testo che avvolgerà la forma.
builder->get_Font()->set_Size(24);
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc->Save(get_ArtifactsDir() + u"Shape.Coordinates.docx");
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
