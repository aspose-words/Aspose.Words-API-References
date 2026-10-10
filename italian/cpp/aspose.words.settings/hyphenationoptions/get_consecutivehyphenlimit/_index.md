---
title: "Metodo Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit"
linktitle: "get_ConsecutiveHyphenLimit"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit. Ottiene o imposta il numero massimo di righe consecutive che possono terminare con trattini. Il valore predefinito per questa proprietà è 0 in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.settings/hyphenationoptions/get_consecutivehyphenlimit/
---
## HyphenationOptions::get_ConsecutiveHyphenLimit method


Ottiene o imposta il numero massimo di righe consecutive che possono terminare con trattini. Il valore predefinito per questa proprietà è 0.

```cpp
int32_t Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit() const
```

## Note


Se il valore di questa proprietà è impostato a 0, qualsiasi numero di righe consecutive può terminare con trattini.

La proprietà non ha effetto quando si salva in formati di pagina fissa, ad es. PDF.

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

* Class [HyphenationOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
