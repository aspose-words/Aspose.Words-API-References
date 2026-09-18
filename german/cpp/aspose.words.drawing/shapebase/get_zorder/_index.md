---
title: "Aspose::Words::Drawing::ShapeBase::get_ZOrder Methode"
linktitle: "get_ZOrder"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_ZOrder Methode. Bestimmt die Anzeigereihenfolge überlappender Formen in C++."
type: docs
weight: 57000
url: /de/cpp/aspose.words.drawing/shapebase/get_zorder/
---
## ShapeBase::get_ZOrder method


Bestimmt die Anzeigereihenfolge überlappender Formen.

```cpp
int32_t Aspose::Words::Drawing::ShapeBase::get_ZOrder()
```

## Hinweise


Wirkt nur bei Formen der obersten Ebene.

Der Standardwert ist 0.

Die Zahl gibt die Stapelreihenfolge an. Eine Form mit einer höheren Zahl wird angezeigt, als ob sie ("Vordergrund" von) einer Form mit einer niedrigeren Zahl liegt.

Die Reihenfolge überlappender Formen ist für Formen in der Kopfzeile und im Haupttext des Dokuments unabhängig.

Die Anzeigereihenfolge von Unterformen in einer Gruppierung wird durch ihre Reihenfolge innerhalb der Gruppe bestimmt.

## Beispiele



Zeigt, wie man die Reihenfolge von Formen manipuliert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie drei unterschiedlich farbige Rechtecke ein, die sich teilweise überlappen.
// Wenn wir eine Form einfügen, die eine andere Form überlappt, platziert Aspose.Words die neuere Form über der älteren.
// Das hellgrüne Rechteck wird das hellblaue Rechteck überlappen und teilweise verdecken,
// und das hellblaue Rechteck wird das orange Rechteck verdecken.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_Orange());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 150, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 150, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 200, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 200, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_LightGreen());

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

// Die "ZOrder"-Eigenschaft einer Form bestimmt ihre Stapelpriorität gegenüber anderen überlappenden Formen.
// Wenn zwei überlappende Formen unterschiedliche "ZOrder"-Werte haben,
// Microsoft Word wird die Form mit dem höheren Wert über die Form mit dem niedrigeren Wert legen.
// Setzen Sie die "ZOrder"-Werte unserer Formen, um das erste orange Rechteck über das zweite hellblaue zu legen
// und das zweite hellblaue Rechteck über das dritte hellgrüne Rechteck.
// Damit wird ihre ursprüngliche Stapelreihenfolge umgekehrt.
shapes[0]->set_ZOrder(3);
shapes[1]->set_ZOrder(2);
shapes[2]->set_ZOrder(1);

doc->Save(get_ArtifactsDir() + u"Shape.ZOrder.docx");
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
