---
title: "Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded metodo"
linktitle: "get_IsSubsettingNeeded"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded. Consente di specificare se il font corrente verrà sottoposto a subset prima di essere esportato come risorsa di font in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.saving/fontsavingargs/get_issubsettingneeded/
---
## FontSavingArgs::get_IsSubsettingNeeded method


Consente di specificare se il carattere corrente sarà ridotto a sottoinsieme prima di essere esportato come risorsa di carattere.

```cpp
bool Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded() const
```

## Note


[Fonts](../../../aspose.words.fonts/) can be exported as complete original font files or subsetted to include only the characters that are used in the document. Subsetting allows to reduce the resulting font resource size.

Per impostazione predefinita, Aspose.Words decide se eseguire il subset confrontando la dimensione del file del font originale con quella specificata in [FontResourcesSubsettingSizeThreshold](../../htmlsaveoptions/get_fontresourcessubsettingsizethreshold/). È possibile sovrascrivere questo comportamento per singoli font impostando la proprietà [IsSubsettingNeeded](./).
## Vedi anche

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
