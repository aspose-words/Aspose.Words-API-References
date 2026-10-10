---
title: "Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit Methode"
linktitle: "get_ConsecutiveHyphenLimit"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit Methode. Gibt den maximalen Wert für die Anzahl aufeinanderfolgender Zeilen zurück, die mit Bindestrichen enden, oder legt ihn fest. Der Standardwert für diese Eigenschaft ist 0 in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.settings/hyphenationoptions/get_consecutivehyphenlimit/
---
## HyphenationOptions::get_ConsecutiveHyphenLimit method


Liest oder setzt die maximale Anzahl aufeinanderfolgender Zeilen, die mit Bindestrichen enden können. Der Standardwert für diese Eigenschaft ist 0.

```cpp
int32_t Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit() const
```

## Hinweise


Wenn der Wert dieser Eigenschaft auf 0 gesetzt wird, kann eine beliebige Anzahl aufeinanderfolgender Zeilen mit Bindestrichen enden.

Die Eigenschaft hat keine Wirkung beim Speichern in feste Seitenformate, z. B. PDF.

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
