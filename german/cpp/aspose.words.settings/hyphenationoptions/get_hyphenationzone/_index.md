---
title: "Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone Methode"
linktitle: "get_HyphenationZone"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone Methode. Liest oder setzt den Abstand in 1/20 Punkt vom rechten Rand, innerhalb dessen Wörter nicht getrennt werden sollen. Der Standardwert für diese Eigenschaft ist 360 (0,25 Zoll) in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.settings/hyphenationoptions/get_hyphenationzone/
---
## HyphenationOptions::get_HyphenationZone method


Liest oder setzt den Abstand in 1/20 Punkt vom rechten Rand, innerhalb dessen Wörter nicht getrennt werden sollen. Der Standardwert für diese Eigenschaft ist 360 (0,25 Zoll).

```cpp
int32_t Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone() const
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
