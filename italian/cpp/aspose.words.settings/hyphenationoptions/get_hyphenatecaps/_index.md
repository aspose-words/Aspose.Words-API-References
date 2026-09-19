---
title: "Metodo Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps"
linktitle: "get_HyphenateCaps"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps. Ottiene o imposta il valore che determina se le parole scritte interamente in maiuscolo sono sillabate. Il valore predefinito per questa proprietà è true in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.settings/hyphenationoptions/get_hyphenatecaps/
---
## HyphenationOptions::get_HyphenateCaps method


Ottiene o imposta il valore che determina se le parole scritte interamente in maiuscolo sono sillabate. Il valore predefinito per questa proprietà è **true**.

```cpp
bool Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps() const
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
