---
title: "Aspose::Words::Drawing::Stroke::get_BackTintAndShade-metod"
linktitle: "get_BackTintAndShade"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Stroke::get_BackTintAndShade-metod. Hämtar eller anger ett dubbelvärde som ljusar upp eller mörkar streckets bakgrundsfärg i C++."
type: docs
weight: 2334
url: /sv/cpp/aspose.words.drawing/stroke/get_backtintandshade/
---
## Stroke::get_BackTintAndShade method


Hämtar eller anger ett dubbelvärde som ljusar upp eller mörkar streckets bakgrundsfärg.

```cpp
double Aspose::Words::Drawing::Stroke::get_BackTintAndShade()
```

## Anmärkningar


De tillåtna värdena ligger inom intervallet från -1 (mörkast) till 1 (ljusast) för denna egenskap. Noll (0) är neutral. Försök att sätta denna egenskap till ett värde mindre än -1 eller större än 1 resulterar i [ArgumentOutOfRangeException](../).

## Exempel



Visar hur man ställer in bakgrundstemat färg samt nyans och skugga.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Stroke gradient outline.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Dark2);
stroke->set_BackTintAndShade(0.2);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeBackThemeColors.docx");
```

## Se även

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
