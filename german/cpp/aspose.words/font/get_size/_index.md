---
title: "Aspose::Words::Font::get_Size Methode"
linktitle: "get_Size"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_Size Methode. Liest oder setzt die Schriftgröße in Punkten in C++."
type: docs
weight: 36000
url: /de/cpp/aspose.words/font/get_size/
---
## Font::get_Size method


Liest oder legt die Schriftgröße in Punkten fest.

```cpp
double Aspose::Words::Font::get_Size()
```


## Beispiele



Zeigt, wie man formatierten Text mit [DocumentBuilder](../../documentbuilder/) einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Geben Sie die Schriftformatierung an und fügen Sie dann Text hinzu.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```


Zeigt, wie man einen Text‑Run mit seiner Schriftarteigenschaft formatiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
