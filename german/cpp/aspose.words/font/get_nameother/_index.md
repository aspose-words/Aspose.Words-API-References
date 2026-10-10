---
title: "Aspose::Words::Font::get_NameOther Methode"
linktitle: "get_NameOther"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_NameOther Methode. Gibt die für Zeichen mit Zeichencodes von 128 bis 255 verwendete Schriftart zurück oder legt sie fest in C++."
type: docs
weight: 29000
url: /de/cpp/aspose.words/font/get_nameother/
---
## Font::get_NameOther method


Gibt die Schriftart zurück oder legt sie fest, die für Zeichen mit Zeichen­codes von 128 bis 255 verwendet wird.

```cpp
System::String Aspose::Words::Font::get_NameOther()
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
