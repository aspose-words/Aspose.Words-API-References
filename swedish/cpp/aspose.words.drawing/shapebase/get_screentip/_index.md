---
title: "Aspose::Words::Drawing::ShapeBase::get_ScreenTip metod"
linktitle: "get_ScreenTip"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_ScreenTip metod. Definierar texten som visas när muspekaren rör sig över formen i C++."
type: docs
weight: 46000
url: /sv/cpp/aspose.words.drawing/shapebase/get_screentip/
---
## ShapeBase::get_ScreenTip method


Definierar texten som visas när muspekaren rör sig över formen.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_ScreenTip()
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
