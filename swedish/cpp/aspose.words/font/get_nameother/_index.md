---
title: "Aspose::Words::Font::get_NameOther metod"
linktitle: "get_NameOther"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_NameOther metod. Returnerar eller anger teckensnittet som används för tecken med teckenkoder från 128 till 255 i C++."
type: docs
weight: 29000
url: /sv/cpp/aspose.words/font/get_nameother/
---
## Font::get_NameOther method


Returnerar eller anger teckensnittet som används för tecken med teckenkoder från 128 till 255.

```cpp
System::String Aspose::Words::Font::get_NameOther()
```


## Exempel



Visar hur Microsoft Word kan kombinera två olika teckensnitt i ett körsegment.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Anta ett körsegment som vi använder byggaren för att infoga medan vi använder den här teckensnittsinställningen
// innehåller tecken inom ASCII-tecknens intervall. I så fall,
// den kommer att visa dessa tecken med detta teckensnitt.
builder->get_Font()->set_NameAscii(u"Calibri");

// Om inget annat teckensnitt anges kommer byggaren också att tillämpa detta teckensnitt på alla tecken som den infogar.
ASSERT_EQ(u"Calibri", builder->get_Font()->get_Name());

// Ange ett teckensnitt att använda för alla tecken utanför ASCII-intervallet.
// Idealiskt bör detta teckensnitt ha en glyf för varje nödvändig icke-ASCII-teckenkod.
builder->get_Font()->set_NameOther(u"Courier New");

// Infoga ett körsegment med ett ord bestående av ASCII-tecken, och ett ord med alla tecken utanför det intervallet.
// Varje tecken kommer att visas med antingen det ena eller det andra teckensnittet, beroende på.
builder->Writeln(u"Hello, Привет");

doc->Save(get_ArtifactsDir() + u"Font.NameAscii.docx");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
