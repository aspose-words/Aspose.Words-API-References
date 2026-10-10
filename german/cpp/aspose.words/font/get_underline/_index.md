---
title: "Aspose::Words::Font::get_Underline Methode"
linktitle: "get_Underline"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_Underline Methode. Gibt den Typ der Unterstreichung zurück oder legt ihn fest, der auf die Schriftart in C++ angewendet wird."
type: docs
weight: 55000
url: /de/cpp/aspose.words/font/get_underline/
---
## Font::get_Underline method


Ruft ab oder legt fest den Typ der Unterstreichung, die auf die Schriftart angewendet wird.

```cpp
Aspose::Words::Underline Aspose::Words::Font::get_Underline()
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


Zeigt, wie man den Stil und die Farbe einer Textunterstreichung konfiguriert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Underline(Aspose::Words::Underline::Dotted);
builder->get_Font()->set_UnderlineColor(System::Drawing::Color::get_Red());

builder->Writeln(u"Underlined text.");

doc->Save(get_ArtifactsDir() + u"Font.Underlines.docx");
```

## Siehe auch

* Enum [Underline](../../underline/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
