---
title: "Aspose::Words::Drawing::Fill::get_Opacity Methode"
linktitle: "get_Opacity"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Fill::get_Opacity Methode. Gibt den Transparenzgrad der angegebenen Füllung zurück oder setzt ihn als Wert zwischen 0,0 (transparent) und 1,0 (undurchsichtig) in C++."
type: docs
weight: 16000
url: /de/cpp/aspose.words.drawing/fill/get_opacity/
---
## Fill::get_Opacity method


Liest oder legt den Grad der Deckkraft der angegebenen Füllung als Wert zwischen 0,0 (klar) und 1,0 (undurchsichtig) fest.

```cpp
double Aspose::Words::Drawing::Fill::get_Opacity()
```


## Beispiele



Zeigt, wie man eine Form mit einer einfarbigen Farbe füllt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Schreiben Sie etwas Text und bedecken Sie ihn anschließend mit einer schwebenden Form.
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::CloudCallout, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 25, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 25, 250, 150, Aspose::Words::Drawing::WrapType::None);

// Verwenden Sie die Eigenschaft \"StrokeColor\", um die Farbe der Kontur der Form festzulegen.
shape->set_StrokeColor(System::Drawing::Color::get_CadetBlue());

// Verwenden Sie die Eigenschaft \"FillColor\", um die Farbe des Innenbereichs der Form festzulegen.
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

// Die Eigenschaft \"Opacity\" bestimmt, wie transparent die Farbe auf einer Skala von 0 bis 1 ist,
// wobei 1 vollständig undurchsichtig und 0 unsichtbar ist.
// Die Füllung der Form ist standardmäßig vollständig undurchsichtig, sodass wir den Text, über dem sich die Form befindet, nicht sehen können.
ASPOSE_ASSERT_EQ(1.0, shape->get_Fill()->get_Opacity());

// Setzen Sie die Opazität der Füllfarbe der Form auf einen niedrigeren Wert, damit wir den darunter liegenden Text sehen können.
shape->get_Fill()->set_Opacity(0.3);

doc->Save(get_ArtifactsDir() + u"Shape.Fill.docx");
```

## Siehe auch

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
