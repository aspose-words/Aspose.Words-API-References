---
title: "Aspose::Words::Drawing::Stroke::get_Color2 Methode"
linktitle: "get_Color2"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Stroke::get_Color2 Methode. Definiert eine zweite Farbe für einen Strich in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.drawing/stroke/get_color2/
---
## Stroke::get_Color2 method


Definiert eine zweite Farbe für einen Strich.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Stroke::get_Color2()
```

## Hinweise


Der Standardwert für ein [Shape](../../shape/) ist **White**.

## Beispiele



Zeigt, wie man Shape‑Strich‑Eigenschaften verarbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();

// Striche können zwei Farben haben, die verwendet werden, um ein Muster zu erzeugen, das durch zweifarbige Bilddaten definiert ist.
// Striche mit einer einzelnen Farbe verwenden die Color2‑Eigenschaft nicht.
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 128, 0, 0), stroke->get_Color());
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 255, 255, 0), stroke->get_Color2());

ASSERT_FALSE(System::TestTools::IsNull(stroke->get_ImageBytes()));
System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Drawing.StrokePattern.png", stroke->get_ImageBytes());
```

## Siehe auch

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
