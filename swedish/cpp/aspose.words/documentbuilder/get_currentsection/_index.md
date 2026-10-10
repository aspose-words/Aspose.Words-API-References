---
title: "Aspose::Words::DocumentBuilder::get_CurrentSection method"
linktitle: "get_CurrentSection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::get_CurrentSection method. Hämtar sektionen som för närvarande är markerad i denna DocumentBuilder i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words/documentbuilder/get_currentsection/
---
## DocumentBuilder::get_CurrentSection method


Hämtar sektionen som för närvarande är markerad i denna [DocumentBuilder](../).

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::DocumentBuilder::get_CurrentSection()
```


## Exempel



Visar hur man infogar en flytande bild och anger dess position och storlek.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Konfigurera figurens egenskap "RelativeHorizontalPosition" så att den behandlar värdet av egenskapen "Left"
// som figurens horisontella avstånd, i punkter, från sidans vänstra kant.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);

// Ställ in figurens horisontella avstånd från sidans vänstra kant till 100.
shape->set_Left(100);

// Använd egenskapen "RelativeVerticalPosition" på liknande sätt för att placera figuren 80pt under sidans övre kant.
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Top(80);

// Ställ in figurens höjd, vilket automatiskt skalar bredden för att bevara proportionerna.
shape->set_Height(125);

ASPOSE_ASSERT_EQ(125.0, shape->get_Width());

// Egenskaperna "Bottom" och "Right" innehåller bildens nedre och högra kanter.
ASPOSE_ASSERT_EQ(shape->get_Top() + shape->get_Height(), shape->get_Bottom());
ASPOSE_ASSERT_EQ(shape->get_Left() + shape->get_Width(), shape->get_Right());

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPositionSize.docx");
```

## Se även

* Class [Section](../../section/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
