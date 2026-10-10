---
title: "Aspose::Words::Font::get_LocaleId-metod"
linktitle: "get_LocaleId"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_LocaleId-metod. Hämtar eller anger språkidentifieraren (språk) för de formaterade tecknen i C++."
type: docs
weight: 22000
url: /sv/cpp/aspose.words/font/get_localeid/
---
## Font::get_LocaleId method


Hämtar eller anger lokalidentifieraren (språk) för de formaterade tecknen.

```cpp
int32_t Aspose::Words::Font::get_LocaleId()
```


## Exempel



Visar hur man anger språket för den text som vi lägger till med en dokumentbyggare.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Om vi ställer in teckensnittets språk till engelska och infogar lite rysk text,
// kommer stavningskontrollen för det engelska språket inte att känna igen texten och markera den som ett stavfel.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());
builder->Writeln(u"Привет!");

// Ställ in ett matchande språk för den text vi ska lägga till för att använda rätt stavningskontroll.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"ru-RU", false)->get_LCID());
builder->Writeln(u"Привет!");

doc->Save(get_ArtifactsDir() + u"Font.LocaleId.docx");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
