---
title: "Aspose::Words::Drawing::Fill::get_ForeTintAndShade metod"
linktitle: "get_ForeTintAndShade"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Fill::get_ForeTintAndShade metod. Hämtar eller anger ett dubbelvärde som ljusar upp eller mörkar förgrundsfärgen i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.drawing/fill/get_foretintandshade/
---
## Fill::get_ForeTintAndShade method


Hämtar eller anger ett dubbelvärde som ljusar upp eller mörkar förgrundsfärgen.

```cpp
double Aspose::Words::Drawing::Fill::get_ForeTintAndShade()
```

## Anmärkningar


De tillåtna värdena ligger i intervallet från -1 (den mörkaste) till 1 (den ljusaste) för denna egenskap.

Noll (0) är neutral.

## Exempel



Visar hur man hanterar ljusning och mörkning av förgrundens teckensnittsfärg.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::SharedPtr<Aspose::Words::Drawing::Fill> textFill = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Fill();
textFill->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
if (textFill->get_ForeTintAndShade() == 0)
{
    textFill->set_ForeTintAndShade(0.5);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillTintAndShade.docx");
```

## Se även

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
