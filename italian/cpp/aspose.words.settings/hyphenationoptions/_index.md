---
title: "Classe Aspose::Words::Settings::HyphenationOptions"
linktitle: "HyphenationOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Settings::HyphenationOptions. Consente di configurare le opzioni di sillabazione del documento. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class


Consente di configurare le opzioni di sillabazione del documento. Per saperne di più, visita l'articolo di documentazione [Lavorare con la sillabazione](https://docs.aspose.com/words/cpp/working-with-hyphenation/).

```cpp
class HyphenationOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_AutoHyphenation](./get_autohyphenation/)() const | Ottiene o imposta il valore che determina se la sillabazione automatica è attivata per il documento. Il valore predefinito per questa proprietà è **false**. |
| [get_ConsecutiveHyphenLimit](./get_consecutivehyphenlimit/)() const | Ottiene o imposta il numero massimo di righe consecutive che possono terminare con trattini. Il valore predefinito per questa proprietà è 0. |
| [get_HyphenateCaps](./get_hyphenatecaps/)() const | Ottiene o imposta il valore che determina se le parole scritte interamente in maiuscolo sono sillabate. Il valore predefinito per questa proprietà è **true**. |
| [get_HyphenationZone](./get_hyphenationzone/)() const | Ottiene o imposta la distanza in 1/20 di punto dal margine destro entro la quale non si desidera sillabare le parole. Il valore predefinito per questa proprietà è 360 (0,25 pollici). |
| [GetType](./gettype/)() const override |  |
| [HyphenationOptions](./hyphenationoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AutoHyphenation](./set_autohyphenation/)(bool) | Impostatore per [Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation](./get_autohyphenation/). |
| [set_ConsecutiveHyphenLimit](./set_consecutivehyphenlimit/)(int32_t) | Impostatore per [Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit](./get_consecutivehyphenlimit/). |
| [set_HyphenateCaps](./set_hyphenatecaps/)(bool) | Impostatore per [Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps](./get_hyphenatecaps/). |
| [set_HyphenationZone](./set_hyphenationzone/)(int32_t) | Impostatore per [Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone](./get_hyphenationzone/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come configurare la sillabazione automatica.
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

## Vedi anche

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
