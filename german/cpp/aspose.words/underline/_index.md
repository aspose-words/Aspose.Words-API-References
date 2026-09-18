---
title: "Aspose::Words::Underline enum"
linktitle: "Underline"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Underline enum. Gibt den Typ der Unterstreichung an, die auf eine Schriftart in C++ angewendet wird."
type: docs
weight: 126000
url: /de/cpp/aspose.words/underline/
---
## Underline enum


Gibt den Typ der Unterstreichung an, die auf eine Schriftart angewendet wird.

```cpp
enum class Underline
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 |  |
| Single | 1 |  |
| Words | 2 |  |
| Double | 3 |  |
| Dotted | 4 |  |
| Thick | 6 |  |
| Dash | 7 |  |
| DashLong | 39 |  |
| DotDash | 9 |  |
| DotDotDash | 10 |  |
| Wavy | 11 |  |
| DottedHeavy | 20 |  |
| DashHeavy | 23 |  |
| DashLongHeavy | 55 |  |
| DotDashHeavy | 25 |  |
| DotDotDashHeavy | 26 |  |
| WavyHeavy | 27 |  |
| WavyDouble | 43 |  |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
