---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes metod"
linktitle: "get_IgnoreFieldCodes"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes metod. Hämtar eller anger ett booleskt värde som indikerar om text inuti fältkoder ska ignoreras. Standardvärdet är false i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefieldcodes/
---
## FindReplaceOptions::get_IgnoreFieldCodes method


Hämtar eller anger ett booleskt värde som indikerar om text inuti fältkoder ska ignoreras. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes() const
```

## Anmärkningar


Det här alternativet påverkar endast fältkoder (det ignorerar inte noder mellan [FieldSeparator](../../../aspose.words/nodetype/) och [FieldEnd](../../../aspose.words/nodetype/)).

För att ignorera hela fältet, använd motsvarande alternativ [IgnoreFields](../get_ignorefields/).

## Exempel



Visar hur man ignorerar text inuti fältkoder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u"INCLUDETEXT", u"Test IT!");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreFieldCodes(ignoreFieldCodes);

// Ersätt 'T' i dokumentet och ignorera text i fältkod eller inte.
doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"T"), u"*", options);
std::cout << doc->GetText() << std::endl;

ASSERT_EQ(ignoreFieldCodes ? System::String(u"\u0013INCLUDETEXT\u0014*est I*!\u0015") : System::String(u"\u0013INCLUDE*EX*\u0014*est I*!\u0015"), doc->GetText().Trim());
```

## Se även

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
