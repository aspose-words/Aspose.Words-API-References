---
title: "Aspose::Words::Font::ClearFormatting-metod"
linktitle: "ClearFormatting"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::ClearFormatting-metod. Återställer till standardteckensnittsformatering i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/font/clearformatting/
---
## Font::ClearFormatting method


Återställer till standardformatering för teckensnitt.

```cpp
void Aspose::Words::Font::ClearFormatting()
```

## Anmärkningar


Tar bort all teckensnittsformatering som specificerats explicit på objektet från vilket [Font](../) erhölls, så att teckensnittsformateringen ärvs från lämplig förälder.

## Exempel



Visar hur man infogar ett hyperlänksfält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Infoga en hyperlänk och betona den med anpassad formatering.
// Hyperlänken kommer att vara en klickbar textbit som tar oss till den plats som anges i URL:en.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Ctrl + vänsterklick på länken i texten i Microsoft Word tar oss till URL:en via ett nytt webbläsarfönster.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
