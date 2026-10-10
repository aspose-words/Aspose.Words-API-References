---
title: "Aspose::Words::Loading::RtfLoadOptions::RtfLoadOptions konstruktor"
linktitle: "RtfLoadOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::RtfLoadOptions::RtfLoadOptions konstruktor. Initierar en ny instans av denna klass med standardvärden i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.loading/rtfloadoptions/rtfloadoptions/
---
## RtfLoadOptions::RtfLoadOptions constructor


Initierar en ny instans av den här klassen med standardvärden.

```cpp
Aspose::Words::Loading::RtfLoadOptions::RtfLoadOptions()
```


## Exempel



Visar hur man upptäcker UTF-8-tecken när man laddar ett RTF-dokument.
```cpp
// Skapa ett "RtfLoadOptions"-objekt för att ändra hur vi laddar ett RTF-dokument.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::RtfLoadOptions>();

// Ställ in egenskapen "RecognizeUtf8Text" till "false" för att anta att dokumentet använder teckenkodningen ISO 8859-1
// och laddar varje tecken i dokumentet.
// Ställ in egenskapen "RecognizeUtf8Text" till "true" för att tolka eventuella variabel-längd tecken som kan förekomma i texten.
loadOptions->set_RecognizeUtf8Text(recognizeUtf8Text);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"UTF-8 characters.rtf", loadOptions);

ASSERT_EQ(recognizeUtf8Text ? System::String(u"“John Doe´s list of currency symbols”™\r") + u"€, ¢, £, ¥, ¤" : System::String(u"â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r") + u"â‚¬, Â¢, Â£, Â¥, Â¤", doc->get_FirstSection()->get_Body()->GetText().Trim());
```

## Se även

* Class [RtfLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
