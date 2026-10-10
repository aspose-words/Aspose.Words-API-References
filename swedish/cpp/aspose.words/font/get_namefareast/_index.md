---
title: "Aspose::Words::Font::get_NameFarEast metod"
linktitle: "get_NameFarEast"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_NameFarEast metod. Returnerar eller anger ett östasiatiskt teckensnittnamn i C++."
type: docs
weight: 28000
url: /sv/cpp/aspose.words/font/get_namefareast/
---
## Font::get_NameFarEast method


Returnerar eller anger ett östasiatiskt teckensnittsnamn.

```cpp
System::String Aspose::Words::Font::get_NameFarEast()
```


## Exempel



Visar hur man infogar och formaterar text på ett östasiatiskt språk.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ange teckensnittsinställningar som dokumentbyggaren kommer att tillämpa på all text som den infogar.
builder->get_Font()->set_Name(u"Courier New");
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());

// Namnge "FarEast"-ekvivalenter för vårt teckensnitt och vår region.
// Om byggaren infogar asiatiska tecken med den här teckensnittskonfigurationen, så kommer varje körning som innehåller
// dessa tecken att visas med "FarEast"-teckensnitt/region istället för standard.
// Detta kan vara användbart när ett västerländskt teckensnitt inte har idealiska representationer för asiatiska tecken.
builder->get_Font()->set_NameFarEast(u"SimSun");
builder->get_Font()->set_LocaleIdFarEast(System::MakeObject<System::Globalization::CultureInfo>(u"zh-CN", false)->get_LCID());

// Den här texten kommer att visas i standardteckensnittet/-regionen.
builder->Writeln(u"Hello world!");

// Eftersom detta är asiatiska tecken kommer den här körningen att tillämpa våra "FarEast"-teckensnitt/region-ekvivalenter.
builder->Writeln(u"你好世界");

doc->Save(get_ArtifactsDir() + u"Font.FarEast.docx");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
