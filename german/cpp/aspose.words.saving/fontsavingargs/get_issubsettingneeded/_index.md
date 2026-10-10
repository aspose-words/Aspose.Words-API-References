---
title: "Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded Methode"
linktitle: "get_IsSubsettingNeeded"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded Methode. Ermöglicht die Angabe, ob die aktuelle Schriftart vor dem Export als Schriftressource in C++ unterteilt wird."
type: docs
weight: 8000
url: /de/cpp/aspose.words.saving/fontsavingargs/get_issubsettingneeded/
---
## FontSavingArgs::get_IsSubsettingNeeded method


Ermöglicht die Angabe, ob die aktuelle Schriftart vor dem Export als Schriftressource teilunterteilt werden soll.

```cpp
bool Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded() const
```

## Hinweise


[Fonts](../../../aspose.words.fonts/) can be exported as complete original font files or subsetted to include only the characters that are used in the document. Subsetting allows to reduce the resulting font resource size.

Standardmäßig entscheidet Aspose.Words, ob ein Subsetting durchgeführt wird, indem es die ursprüngliche Schriftdateigröße mit der in [FontResourcesSubsettingSizeThreshold](../../htmlsaveoptions/get_fontresourcessubsettingsizethreshold/) angegebenen vergleicht. Sie können dieses Verhalten für einzelne Schriftarten überschreiben, indem Sie die Eigenschaft [IsSubsettingNeeded](./) setzen.
## Siehe auch

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
