---
title: "Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps Methode"
linktitle: "get_HyphenateCaps"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps Methode. Liest oder setzt den Wert, der bestimmt, ob Wörter, die vollständig in Großbuchstaben geschrieben sind, getrennt werden. Der Standardwert für diese Eigenschaft ist true in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.settings/hyphenationoptions/get_hyphenatecaps/
---
## HyphenationOptions::get_HyphenateCaps method


Liest oder setzt den Wert, der bestimmt, ob Wörter, die komplett in Großbuchstaben geschrieben sind, getrennt werden. Der Standardwert für diese Eigenschaft ist **true**.

```cpp
bool Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps() const
```


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

* Class [HyphenationOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
