---
title: "Aspose::Words::Layout::ContinuousSectionRestart enum"
linktitle: "ContinuousSectionRestart"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Layout::ContinuousSectionRestart enum. Representerar olika beteenden när sidnummer beräknas i ett kontinuerligt avsnitt som startar om sidnumrering i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enum


Representerar olika beteenden när sidnummer beräknas i ett kontinuerligt avsnitt som startar om sidnumreringen.

```cpp
enum class ContinuousSectionRestart
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Alltid | 0 | Sidnumrering startar alltid om oavsett innehållsflöde. |
| FromNewPageOnly | 1 | Sidnumrering startar om endast om det inte finns något annat innehåll före avsnittet på sidan där avsnittet börjar. |


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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
