---
title: "Aspose::Words::Font::get_Spacing metod"
linktitle: "get_Spacing"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_Spacing metod. Returnerar eller anger avståndet (i punkter) mellan tecken i C++."
type: docs
weight: 40000
url: /sv/cpp/aspose.words/font/get_spacing/
---
## Font::get_Spacing method


Returnerar eller anger avståndet (i punkter) mellan tecken.

```cpp
double Aspose::Words::Font::get_Spacing()
```


## Exempel



Visar hur man ställer in horisontell skalning och avstånd för tecken.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Lägg till en textsekvens och öka teckenbredden till 150 %.
builder->get_Font()->set_Scaling(150);
builder->Writeln(u"Wide characters");

// Lägg till en textsekvens och lägg till 1 pt extra horisontellt avstånd mellan varje tecken.
builder->get_Font()->set_Spacing(1);
builder->Writeln(u"Expanded by 1pt");

// Lägg till en textsekvens och för tecknen närmare varandra med 1 pt.
builder->get_Font()->set_Spacing(-1);
builder->Writeln(u"Condensed by 1pt");

doc->Save(get_ArtifactsDir() + u"Font.ScalingSpacing.docx");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
