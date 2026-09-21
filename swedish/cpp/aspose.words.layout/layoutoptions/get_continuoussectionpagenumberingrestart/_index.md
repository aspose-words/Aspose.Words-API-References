---
title: "Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart metod"
linktitle: "get_ContinuousSectionPageNumberingRestart"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart metod. Hämtar eller anger läget för beteende vid beräkning av sidnummer när ett kontinuerligt avsnitt startar om sidnumreringen i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.layout/layoutoptions/get_continuoussectionpagenumberingrestart/
---
## LayoutOptions::get_ContinuousSectionPageNumberingRestart method


Hämtar eller sätter beteendemodet för beräkning av sidnummer när ett kontinuerligt avsnitt startar om sidnumreringen.

```cpp
Aspose::Words::Layout::ContinuousSectionRestart Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart() const
```


## Exempel



Visar hur man styr sidnumrering i ett kontinuerligt avsnitt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Continuous section page numbering.docx");

// Som standard matchar Aspose.Words beteende Microsoft Word 2019.
// Om du behöver det gamla Aspose.Words‑beteendet, likt Microsoft Word 2016, använd 'ContinuousSectionRestart.FromNewPageOnly'.
// Sidnumrering startar om endast om det inte finns något annat innehåll före avsnittet på sidan där avsnittet börjar,
// på grund av detta kommer numreringen att återställas till 2 från den andra sidan.
doc->get_LayoutOptions()->set_ContinuousSectionPageNumberingRestart(Aspose::Words::Layout::ContinuousSectionRestart::FromNewPageOnly);
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Layout.RestartPageNumberingInContinuousSection.pdf");
```

## Se även

* Enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
