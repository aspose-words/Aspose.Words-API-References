---
title: "Aspose::Words::Drawing::ShapeBase::get_Target metod"
linktitle: "get_Target"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_Target metod. Hämtar eller anger målramen för formens hyperlänk i C++."
type: docs
weight: 50000
url: /sv/cpp/aspose.words.drawing/shapebase/get_target/
---
## ShapeBase::get_Target method


Hämtar eller anger målramen för formens hyperlänk.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_Target()
```

## Anmärkningar


Standardvärdet är en tom sträng.

## Exempel



Visar hur man infogar en form som innehåller en bild och också är en hyperlänk.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_HRef(u"https://forum.aspose.com/");
shape->set_Target(u"New Window");
shape->set_ScreenTip(u"Aspose.Words Support Forums");

// Ctrl + vänsterklick på formen i Microsoft Word öppnar ett nytt webbläsarfönster
// och tar oss till hyperlänken i egenskapen "HRef".
doc->Save(get_ArtifactsDir() + u"Image.InsertImageWithHyperlink.docx");
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
