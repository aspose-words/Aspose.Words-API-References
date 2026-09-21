---
title: "Aspose::Words::Drawing::ShapeBase::get_Name‑metod"
linktitle: "get_Name"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_Name‑metod. Hämtar eller anger det valfria formnamnet i C++."
type: docs
weight: 40000
url: /sv/cpp/aspose.words.drawing/shapebase/get_name/
---
## ShapeBase::get_Name method


Hämtar eller anger det valfria namnet på formen.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_Name()
```

## Anmärkningar


Standard är en tom sträng.

Kan inte vara **null**, men kan vara en tom sträng.

## Exempel



Visar hur man använder en forms alternativa text.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 150, 150);
shape->set_Name(u"MyCube");

shape->set_AlternativeText(u"Alt text for MyCube.");

// Vi kan komma åt den alternativa texten för en form genom att högerklicka på den och sedan via "Format AutoShape" -> "Alt Text".
doc->Save(get_ArtifactsDir() + u"Shape.AltText.docx");

// Spara dokumentet som HTML och ta sedan bort den länkade bilden som tillhör vår form.
// Webbläsaren som läser vår HTML kommer att visa alt‑texten i stället för den saknade bilden.
doc->Save(get_ArtifactsDir() + u"Shape.AltText.html");
System::IO::File::Delete(get_ArtifactsDir() + u"Shape.AltText.001.png");
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
