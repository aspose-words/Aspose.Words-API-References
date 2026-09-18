---
title: "Aspose::Words::Font::get_LocaleId Methode"
linktitle: "get_LocaleId"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_LocaleId Methode. Gibt den Gebietsschema‑Bezeichner (Sprache) der formatierten Zeichen zurück oder legt ihn in C++ fest."
type: docs
weight: 22000
url: /de/cpp/aspose.words/font/get_localeid/
---
## Font::get_LocaleId method


Liest oder setzt die Gebietsschema‑Kennung (Sprache) der formatierten Zeichen.

```cpp
int32_t Aspose::Words::Font::get_LocaleId()
```


## Beispiele



Zeigt, wie das Gebietsschema des Textes festgelegt wird, den wir mit einem Document Builder hinzufügen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Wenn wir das Gebietsschema der Schriftart auf Englisch setzen und etwas russischen Text einfügen,
// wird die Rechtschreibprüfung für das englische Gebietsschema den Text nicht erkennen und ihn als Rechtschreibfehler markieren.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());
builder->Writeln(u"Привет!");

// Legen Sie ein passendes Gebietsschema für den Text fest, den wir hinzufügen wollen, um die entsprechende Rechtschreibprüfung anzuwenden.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"ru-RU", false)->get_LCID());
builder->Writeln(u"Привет!");

doc->Save(get_ArtifactsDir() + u"Font.LocaleId.docx");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
