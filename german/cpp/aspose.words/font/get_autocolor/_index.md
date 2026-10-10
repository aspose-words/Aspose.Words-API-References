---
title: "Aspose::Words::Font::get_AutoColor Methode"
linktitle: "get_AutoColor"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_AutoColor-Methode. Gibt die aktuell berechnete Farbe des Textes (schwarz oder weiß) zurück, die für ''auto color'' verwendet wird. Wenn die Farbe nicht ''auto'' ist, wird Color in C++ zurückgegeben."
type: docs
weight: 4000
url: /de/cpp/aspose.words/font/get_autocolor/
---
## Font::get_AutoColor method


Gibt die aktuell berechnete Farbe des Textes (schwarz oder weiß) zurück, die für 'auto color' verwendet wird. Wenn die Farbe nicht 'auto' ist, wird [Color](../get_color/) zurückgegeben.

```cpp
System::Drawing::Color Aspose::Words::Font::get_AutoColor()
```

## Hinweise


Wenn Text die 'automatische Farbe' hat, wird die tatsächliche Textfarbe automatisch berechnet, sodass sie vor der Hintergrundfarbe lesbar ist. Wenn Sie die Hintergrundfarbe ändern, wechselt die Textfarbe in MS Word automatisch zu Schwarz oder Weiß, um die Lesbarkeit zu maximieren.

## Beispiele



Zeigt, wie die Lesbarkeit verbessert werden kann, indem die Textfarbe automatisch basierend auf der Helligkeit des Hintergrunds ausgewählt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Wenn das Font-Objekt eines Laufes keine Textfarbe angibt, wird es automatisch
// wählt entweder Schwarz oder Weiß abhängig von der Farbe des Hintergrunds.
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());

// Die Standardfarbe für Text ist Schwarz. Wenn die Hintergrundfarbe dunkel ist, wird schwarzer Text schwer zu sehen sein.
// Um dieses Problem zu lösen, zeigt die AutoColor-Eigenschaft diesen Text in Weiß an.
builder->get_Font()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_DarkBlue());

builder->Writeln(u"The text color automatically chosen for this run is white.");

ASSERT_EQ(System::Drawing::Color::get_White().ToArgb(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_AutoColor().ToArgb());

// Wenn wir den Hintergrund zu einer hellen Farbe ändern, wird Schwarz ein
// geeigneterer Textfarbe als Weiß sein, sodass die AutoColor es in Schwarz darstellt.
builder->get_Font()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());

builder->Writeln(u"The text color automatically chosen for this run is black.");

ASSERT_EQ(System::Drawing::Color::get_Black().ToArgb(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_Runs()->idx_get(0)->get_Font()->get_AutoColor().ToArgb());

doc->Save(get_ArtifactsDir() + u"Font.SetFontAutoColor.docx");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
