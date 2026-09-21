---
title: "Aspose::Words::Border::get_TintAndShade metod"
linktitle: "get_TintAndShade"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Border::get_TintAndShade metod. Hämtar eller anger ett dubbelvärde som ljusar upp eller mörkar en färg i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words/border/get_tintandshade/
---
## Border::get_TintAndShade method


Hämtar eller anger ett dubbelvärde som ljusar upp eller mörkar en färg.

```cpp
double Aspose::Words::Border::get_TintAndShade()
```

## Anmärkningar


De tillåtna värdena ligger i intervallet från -1 (mörkast) till 1 (ljusast) för denna egenskap. Noll (0) är neutral.

## Exempel



Visar hur man infogar ett stycke med en övre kant.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// Ställ in ThemeColor endast när LineWidth eller LineStyle har satts.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## Se även

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
