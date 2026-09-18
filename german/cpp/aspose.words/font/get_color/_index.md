---
title: "Aspose::Words::Font::get_Color Methode"
linktitle: "get_Color"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_Color Methode. Liest oder setzt die Farbe der Schriftart in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words/font/get_color/
---
## Font::get_Color method


Liest oder setzt die Farbe der Schrift.

```cpp
System::Drawing::Color Aspose::Words::Font::get_Color()
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


Zeigt, wie man ein Hyperlink-Feld einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Fügen Sie einen Hyperlink ein und heben Sie ihn mit benutzerdefinierter Formatierung hervor.
// Der Hyperlink wird ein anklickbarer Text sein, der uns zu dem in der URL angegebenen Ort führt.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Strg + Linksklick auf den Link im Text in Microsoft Word öffnet die URL in einem neuen Webbrowser-Fenster.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
