---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes metod"
linktitle: "get_IgnoreFootnotes"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes metod. Hämtar eller anger ett booleskt värde som indikerar om fotnoter ska ignoreras. Standardvärdet är false i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefootnotes/
---
## FindReplaceOptions::get_IgnoreFootnotes method


Hämtar eller anger ett booleskt värde som indikerar om fotnoter ska ignoreras. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes() const
```


## Exempel



Visar hur man ignorerar fotnoter under en sök‑och‑ersätt‑operation.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder->InsertParagraph();

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Ställ in flaggan "IgnoreFootnotes" till "true" för att utföra sök‑och‑ersätt
// operationen för att ignorera text i fotnoter.
// Ställ in flaggan "IgnoreFootnotes" till "false" för att utföra sök‑och‑ersätt
// operationen för att även söka efter text i fotnoter.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreFootnotes(isIgnoreFootnotes);
doc->get_Range()->Replace(u"Lorem ipsum", u"Replaced Lorem ipsum", options);
```

## Se även

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
