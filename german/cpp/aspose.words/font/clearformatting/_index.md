---
title: "Aspose::Words::Font::ClearFormatting-Methode"
linktitle: "ClearFormatting"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::ClearFormatting-Methode. Setzt die Schriftformatierung in C++ auf die Standardwerte zurück."
type: docs
weight: 2000
url: /de/cpp/aspose.words/font/clearformatting/
---
## Font::ClearFormatting method


Setzt die Schriftformatierung auf die Standardwerte zurück.

```cpp
void Aspose::Words::Font::ClearFormatting()
```

## Hinweise


Entfernt alle Schriftformatierungen, die explizit auf dem Objekt angegeben wurden, von dem [Font](../) erhalten wurde, sodass die Schriftformatierung vom entsprechenden übergeordneten Element geerbt wird.

## Beispiele



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
