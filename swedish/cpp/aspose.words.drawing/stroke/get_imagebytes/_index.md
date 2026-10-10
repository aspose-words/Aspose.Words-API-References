---
title: "Aspose::Words::Drawing::Stroke::get_ImageBytes metod"
linktitle: "get_ImageBytes"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Stroke::get_ImageBytes metod. Definierar bilden för en linjebilduppläggning eller mönsterfyllning i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.drawing/stroke/get_imagebytes/
---
## Stroke::get_ImageBytes method


Definierar bilden för en streckbild eller mönsterfyllning.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::Stroke::get_ImageBytes()
```


## Exempel



Visar hur man bearbetar shape-stroke-funktioner.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();

// Strokes kan ha två färger, vilka används för att skapa ett mönster definierat av tvåtonig bilddata.
// Strokes med en enda färg använder inte egenskapen Color2.
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 128, 0, 0), stroke->get_Color());
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 255, 255, 0), stroke->get_Color2());

ASSERT_FALSE(System::TestTools::IsNull(stroke->get_ImageBytes()));
System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Drawing.StrokePattern.png", stroke->get_ImageBytes());
```

## Se även

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
