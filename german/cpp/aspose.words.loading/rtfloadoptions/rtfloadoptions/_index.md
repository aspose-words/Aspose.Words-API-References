---
title: "Aspose::Words::Loading::RtfLoadOptions::RtfLoadOptions‑Konstruktor"
linktitle: "RtfLoadOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::RtfLoadOptions::RtfLoadOptions‑Konstruktor. Initialisiert eine neue Instanz dieser Klasse mit Standardwerten in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.loading/rtfloadoptions/rtfloadoptions/
---
## RtfLoadOptions::RtfLoadOptions constructor


Initialisiert eine neue Instanz dieser Klasse mit Standardwerten.

```cpp
Aspose::Words::Loading::RtfLoadOptions::RtfLoadOptions()
```


## Beispiele



Zeigt, wie man UTF‑8‑Zeichen beim Laden eines RTF‑Dokuments erkennt.
```cpp
// Erstellen Sie ein "RtfLoadOptions"-Objekt, um zu ändern, wie wir ein RTF-Dokument laden.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::RtfLoadOptions>();

// Setzen Sie die Eigenschaft "RecognizeUtf8Text" auf "false", um anzunehmen, dass das Dokument den ISO‑8859‑1‑Zeichensatz verwendet.
// und lädt jedes Zeichen im Dokument.
// Setzen Sie die Eigenschaft "RecognizeUtf8Text" auf "true", um beliebige variabel lange Zeichen zu analysieren, die im Text vorkommen können.
loadOptions->set_RecognizeUtf8Text(recognizeUtf8Text);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"UTF-8 characters.rtf", loadOptions);

ASSERT_EQ(recognizeUtf8Text ? System::String(u"“John Doe´s list of currency symbols”™\r") + u"€, ¢, £, ¥, ¤" : System::String(u"â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r") + u"â‚¬, Â¢, Â£, Â¥, Â¤", doc->get_FirstSection()->get_Body()->GetText().Trim());
```

## Siehe auch

* Class [RtfLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
