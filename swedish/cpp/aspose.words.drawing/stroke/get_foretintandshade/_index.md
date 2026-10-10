---
title: "Aspose::Words::Drawing::Stroke::get_ForeTintAndShade metod"
linktitle: "get_ForeTintAndShade"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Stroke::get_ForeTintAndShade metod. Hämtar eller anger ett dubbelvärde som ljusar upp eller mörkar streckets förgrundsfärg i C++."
type: docs
weight: 10667
url: /sv/cpp/aspose.words.drawing/stroke/get_foretintandshade/
---
## Stroke::get_ForeTintAndShade method


Hämtar eller anger ett dubbelvärde som ljusar upp eller mörkar streckets förgrundsfärg.

```cpp
double Aspose::Words::Drawing::Stroke::get_ForeTintAndShade()
```

## Anmärkningar


De tillåtna värdena ligger inom intervallet från -1 (mörkast) till 1 (ljusast) för denna egenskap. Noll (0) är neutral. Försök att sätta denna egenskap till ett värde mindre än -1 eller större än 1 resulterar i [ArgumentOutOfRangeException](../).

## Exempel



Visar hur man anger förgrundstemat färg samt nyans och skugga.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 40);
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
stroke->set_ForeTintAndShade(0.5);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeForeThemeColors.docx");
```

## Se även

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
