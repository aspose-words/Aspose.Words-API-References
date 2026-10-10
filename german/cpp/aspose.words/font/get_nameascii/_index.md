---
title: "Aspose::Words::Font::get_NameAscii Methode"
linktitle: "get_NameAscii"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_NameAscii Methode. Gibt die für lateinischen Text (Zeichen mit Zeichen­codes von 0 (null) bis 127) verwendete Schriftart zurück oder legt sie fest in C++."
type: docs
weight: 26000
url: /de/cpp/aspose.words/font/get_nameascii/
---
## Font::get_NameAscii method


Gibt die Schriftart zurück oder legt sie fest, die für lateinischen Text verwendet wird (Zeichen mit Zeichen­codes von 0 (null) bis 127).

```cpp
System::String Aspose::Words::Font::get_NameAscii()
```


## Beispiele



Zeigt, wie Microsoft Word zwei verschiedene Schriftarten in einem Lauf kombinieren kann.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Angenommen, ein Lauf, den wir mit dem Builder einfügen, während wir diese Schriftartkonfiguration verwenden.
// enthält Zeichen im ASCII‑Zeichenbereich. In diesem Fall,
// wird diese Zeichen mit dieser Schriftart anzeigen.
builder->get_Font()->set_NameAscii(u"Calibri");

// Wenn keine andere Schriftart angegeben ist, wendet der Builder diese Schriftart ebenfalls auf alle Zeichen an, die er einfügt.
ASSERT_EQ(u"Calibri", builder->get_Font()->get_Name());

// Geben Sie eine Schriftart an, die für alle Zeichen außerhalb des ASCII‑Bereichs verwendet werden soll.
// Idealerweise sollte diese Schriftart für jeden erforderlichen Nicht‑ASCII‑Zeichencode ein Glyph besitzen.
builder->get_Font()->set_NameOther(u"Courier New");

// Fügen Sie einen Lauf ein, der ein Wort aus ASCII‑Zeichen enthält, und ein Wort, das alle Zeichen außerhalb dieses Bereichs enthält.
// Jedes Zeichen wird je nach Situation mit einer der beiden Schriftarten angezeigt.
builder->Writeln(u"Hello, Привет");

doc->Save(get_ArtifactsDir() + u"Font.NameAscii.docx");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
