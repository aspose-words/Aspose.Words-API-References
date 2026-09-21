---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml metod"
linktitle: "get_SupportVml"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml metod. Hämtar eller anger ett värde som indikerar om VML-bilder ska stödjas i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.loading/htmlloadoptions/get_supportvml/
---
## HtmlLoadOptions::get_SupportVml method


Hämtar eller anger ett värde som indikerar om VML-bilder ska stödjas.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml() const
```


## Exempel



Visar hur man stödjer villkorliga kommentarer vid inläsning av ett HTML-dokument.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// Om värdet är sant, tar vi VML-kod i beaktande när vi parsar det laddade dokumentet.
loadOptions->set_SupportVml(supportVml);

// Detta dokument innehåller en JPEG-bild inom "<!--[if gte vml 1]>"-taggar,
// och en annan PNG-bild inom "<![if !vml]>"-taggar.
// Om vi sätter flaggan "SupportVml" till "true" kommer Aspose.Words att ladda JPEG-filen.
// Om vi sätter denna flagga till "false" kommer Aspose.Words endast att ladda PNG-filen.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## Se även

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
