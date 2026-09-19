---
title: "metodo Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone"
linktitle: "get_HyphenationZone"
second_title: "Riferimento API Aspose.Words per C++"
description: "metodo Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone. Ottiene o imposta la distanza in 1/20 di punto dal margine destro entro la quale non si desidera sillabare le parole. Il valore predefinito per questa proprietà è 360 (0,25 pollice) in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.settings/hyphenationoptions/get_hyphenationzone/
---
## HyphenationOptions::get_HyphenationZone method


Ottiene o imposta la distanza in 1/20 di punto dal margine destro entro la quale non si desidera sillabare le parole. Il valore predefinito per questa proprietà è 360 (0,25 pollici).

```cpp
int32_t Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone() const
```


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
