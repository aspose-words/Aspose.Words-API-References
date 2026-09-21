---
title: "Aspose::Words::Font::get_NameBi metod"
linktitle: "get_NameBi"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_NameBi metod. Returnerar eller anger namnet på teckensnittet i ett dokument på ett språk som skrivs från höger till vänster i C++."
type: docs
weight: 27000
url: /sv/cpp/aspose.words/font/get_namebi/
---
## Font::get_NameBi method


Returnerar eller anger namnet på teckensnittet i ett språkdokument som skrivs från höger till vänster.

```cpp
System::String Aspose::Words::Font::get_NameBi()
```


## Exempel



Visar hur man definierar separata uppsättningar av teckensnittinställningar för höger-till-vänster, och höger-till-vänster-text.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Definiera en uppsättning teckensnittinställningar för vänster-till-höger-text.
builder->get_Font()->set_Name(u"Courier New");
builder->get_Font()->set_Size(16);
builder->get_Font()->set_Italic(false);
builder->get_Font()->set_Bold(false);
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());

// Definiera en annan uppsättning teckensnittinställningar för höger-till-vänster-text.
builder->get_Font()->set_NameBi(u"Andalus");
builder->get_Font()->set_SizeBi(24);
builder->get_Font()->set_ItalicBi(true);
builder->get_Font()->set_BoldBi(true);
builder->get_Font()->set_LocaleIdBi(System::MakeObject<System::Globalization::CultureInfo>(u"ar-AR", false)->get_LCID());

// Vi kan använda Bidi-flaggan för att indikera om texten vi håller på att lägga till
// med dokumentbyggaren är från höger till vänster. När vi lägger till text med denna flagga satt till true,
// den kommer att formateras med den från höger till vänster uppsättningen av teckensnittsinställningar.
builder->get_Font()->set_Bidi(true);
builder->Write(u"مرحبًا");

// Ställ in flaggan till false, och lägg sedan till text från vänster till höger.
// Dokumentbyggaren kommer att formatera dessa med den från vänster till höger uppsättningen av teckensnittsinställningar.
builder->get_Font()->set_Bidi(false);
builder->Write(u" Hello world!");

doc->Save(get_ArtifactsDir() + u"Font.Bidi.docx");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
