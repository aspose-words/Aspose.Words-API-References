---
title: "Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded метод"
linktitle: "get_IsSubsettingNeeded"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded. Позволяет указать, будет ли текущий шрифт подмножен перед экспортом в виде ресурса шрифта в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.saving/fontsavingargs/get_issubsettingneeded/
---
## FontSavingArgs::get_IsSubsettingNeeded method


Позволяет указать, будет ли текущий шрифт подмножеством перед экспортом в виде ресурса шрифта.

```cpp
bool Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded() const
```

## Примечания


[Fonts](../../../aspose.words.fonts/) can be exported as complete original font files or subsetted to include only the characters that are used in the document. Subsetting allows to reduce the resulting font resource size.

По умолчанию Aspose.Words определяет, выполнять ли подмножество, сравнивая исходный размер файла шрифта с размером, указанным в [FontResourcesSubsettingSizeThreshold](../../htmlsaveoptions/get_fontresourcessubsettingsizethreshold/). Вы можете переопределить это поведение для отдельных шрифтов, установив свойство [IsSubsettingNeeded](./).
## См. также

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
