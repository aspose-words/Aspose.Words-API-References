---
title: "Aspose::Words::Font::get_NameFarEast Methode"
linktitle: "get_NameFarEast"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_NameFarEast Methode. Gibt einen ostasiatischen Schriftartnamen zurück oder legt ihn fest in C++."
type: docs
weight: 28000
url: /de/cpp/aspose.words/font/get_namefareast/
---
## Font::get_NameFarEast method


Gibt einen ostasiatischen Schriftartnamen zurück oder legt ihn fest.

```cpp
System::String Aspose::Words::Font::get_NameFarEast()
```


## Beispiele



Zeigt, wie man Text in einer fernöstlichen Sprache einfügt und formatiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Geben Sie Schriftarteinstellungen an, die der Dokumenten‑Builder auf jeden eingefügten Text anwendet.
builder->get_Font()->set_Name(u"Courier New");
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());

// Benennen Sie die "FarEast"‑Entsprechungen für unsere Schriftart und das Gebietsschema.
// Wenn der Builder asiatische Zeichen mit dieser Schriftart‑Konfiguration einfügt, dann enthält jeder Lauf, der
// diese Zeichen werden mit der "FarEast"‑Schriftart/Gebietsschema anstelle der Vorgabe angezeigt.
// Dies kann nützlich sein, wenn eine westliche Schriftart keine idealen Darstellungen für asiatische Zeichen bietet.
builder->get_Font()->set_NameFarEast(u"SimSun");
builder->get_Font()->set_LocaleIdFarEast(System::MakeObject<System::Globalization::CultureInfo>(u"zh-CN", false)->get_LCID());

// Dieser Text wird in der Standard‑Schriftart/dem Standard‑Gebietsschema angezeigt.
builder->Writeln(u"Hello world!");

// Da es sich um asiatische Zeichen handelt, wird dieser Lauf unsere "FarEast"‑Schriftart/Gebietsschema‑Entsprechungen anwenden.
builder->Writeln(u"你好世界");

doc->Save(get_ArtifactsDir() + u"Font.FarEast.docx");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
