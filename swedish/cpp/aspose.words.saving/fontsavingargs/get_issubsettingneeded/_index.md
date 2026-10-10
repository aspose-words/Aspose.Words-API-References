---
title: "Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded‑metoden"
linktitle: "get_IsSubsettingNeeded"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded‑metoden. Tillåter att ange om det aktuella teckensnittet ska subsettas innan export som en teckensnittresurs i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.saving/fontsavingargs/get_issubsettingneeded/
---
## FontSavingArgs::get_IsSubsettingNeeded method


Tillåter att ange om det aktuella teckensnittet ska delmängdas innan export som en teckensnittresurs.

```cpp
bool Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded() const
```

## Anmärkningar


[Fonts](../../../aspose.words.fonts/) can be exported as complete original font files or subsetted to include only the characters that are used in the document. Subsetting allows to reduce the resulting font resource size.

Som standard avgör Aspose.Words om subsetting ska utföras genom att jämföra den ursprungliga teckensnittets filstorlek med den som anges i [FontResourcesSubsettingSizeThreshold](../../htmlsaveoptions/get_fontresourcessubsettingsizethreshold/). Du kan åsidosätta detta beteende för enskilda teckensnitt genom att sätta egenskapen [IsSubsettingNeeded](./).
## Se även

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
