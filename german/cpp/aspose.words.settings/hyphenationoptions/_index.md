---
title: "Aspose::Words::Settings::HyphenationOptions Klasse"
linktitle: "HyphenationOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::HyphenationOptions Klasse. Ermöglicht die Konfiguration von Silbentrennungsoptionen für das Dokument. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class


Ermöglicht die Konfiguration von Silbentrennungsoptionen für das Dokument. Weitere Informationen finden Sie im Dokumentationsartikel [Arbeiten mit Silbentrennung](https://docs.aspose.com/words/cpp/working-with-hyphenation/).

```cpp
class HyphenationOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_AutoHyphenation](./get_autohyphenation/)() const | Liest oder setzt den Wert, der bestimmt, ob die automatische Silbentrennung für das Dokument aktiviert ist. Der Standardwert für diese Eigenschaft ist **false**. |
| [get_ConsecutiveHyphenLimit](./get_consecutivehyphenlimit/)() const | Liest oder setzt die maximale Anzahl aufeinanderfolgender Zeilen, die mit Bindestrichen enden können. Der Standardwert für diese Eigenschaft ist 0. |
| [get_HyphenateCaps](./get_hyphenatecaps/)() const | Liest oder setzt den Wert, der bestimmt, ob Wörter, die komplett in Großbuchstaben geschrieben sind, getrennt werden. Der Standardwert für diese Eigenschaft ist **true**. |
| [get_HyphenationZone](./get_hyphenationzone/)() const | Liest oder setzt den Abstand in 1/20 Punkt vom rechten Rand, innerhalb dessen Wörter nicht getrennt werden sollen. Der Standardwert für diese Eigenschaft ist 360 (0,25 Zoll). |
| [GetType](./gettype/)() const override |  |
| [HyphenationOptions](./hyphenationoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AutoHyphenation](./set_autohyphenation/)(bool) | Setter für [Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation](./get_autohyphenation/). |
| [set_ConsecutiveHyphenLimit](./set_consecutivehyphenlimit/)(int32_t) | Setter für [Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit](./get_consecutivehyphenlimit/). |
| [set_HyphenateCaps](./set_hyphenatecaps/)(bool) | Setter für [Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps](./get_hyphenatecaps/). |
| [set_HyphenationZone](./set_hyphenationzone/)(int32_t) | Setter für [Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone](./get_hyphenationzone/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie die automatische Silbentrennung konfiguriert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(24);
builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->get_HyphenationOptions()->set_AutoHyphenation(true);
doc->get_HyphenationOptions()->set_ConsecutiveHyphenLimit(2);
doc->get_HyphenationOptions()->set_HyphenationZone(720);
doc->get_HyphenationOptions()->set_HyphenateCaps(true);

doc->Save(get_ArtifactsDir() + u"Document.HyphenationOptions.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
