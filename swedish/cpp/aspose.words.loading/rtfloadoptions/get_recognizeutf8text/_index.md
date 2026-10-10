---
title: "Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text metod"
linktitle: "get_RecognizeUtf8Text"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text metod. När den är satt till true kommer den att försöka upptäcka UTF8-tecken, de kommer att bevaras under import i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.loading/rtfloadoptions/get_recognizeutf8text/
---
## RtfLoadOptions::get_RecognizeUtf8Text method


När den är inställd på **true**, kommer den att försöka upptäcka UTF8-tecken, de kommer att bevaras under import.

```cpp
bool Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text() const
```

## Anmärkningar


Standardvärdet är **false**.

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
