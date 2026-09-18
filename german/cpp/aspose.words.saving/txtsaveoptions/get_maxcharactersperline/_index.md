---
title: "Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine-Methode"
linktitle: "get_MaxCharactersPerLine"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine-Methode. Gibt einen ganzzahligen Wert zurück oder setzt ihn, der die maximale Anzahl von Zeichen pro Zeile angibt. Der Standardwert ist 0, was in C++ kein Limit bedeutet."
type: docs
weight: 5000
url: /de/cpp/aspose.words.saving/txtsaveoptions/get_maxcharactersperline/
---
## TxtSaveOptions::get_MaxCharactersPerLine method


Liefert oder setzt einen ganzzahligen Wert, der die maximale Anzahl von Zeichen pro Zeile angibt. Der Standardwert ist 0, was kein Limit bedeutet.

```cpp
int32_t Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine() const
```


## Beispiele



Zeigt, wie die maximale Zeichenanzahl pro Zeile festgelegt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Setzen Sie 30 Zeichen als maximal zulässige Anzahl pro Zeile.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_MaxCharactersPerLine(30);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.MaxCharactersPerLine.txt", saveOptions);
```

## Siehe auch

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
