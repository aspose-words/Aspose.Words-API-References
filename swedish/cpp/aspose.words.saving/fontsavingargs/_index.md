---
title: "Aspose::Words::Saving::FontSavingArgs class"
linktitle: "FontSavingArgs"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::FontSavingArgs class. Tillhandahåller data för FontSaving()-händelsen. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class


Tillhandahåller data för [FontSaving()](../ifontsavingcallback/fontsaving/)‑händelsen. För att lära dig mer, besök dokumentationsartikeln [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class FontSavingArgs : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Bold](./get_bold/)() const | Anger om det aktuella teckensnittet är fetstil. |
| [get_Document](./get_document/)() const | Hämtar dokumentobjektet som sparas. |
| [get_FontFamilyName](./get_fontfamilyname/)() const | Anger det aktuella teckensnittsfamiljenamnet. |
| [get_FontFileName](./get_fontfilename/)() const | Hämtar eller anger filnamnet (utan sökväg) där teckensnittet ska sparas till. |
| [get_FontStream](./get_fontstream/)() const | Tillåter att ange strömmen där teckensnittet ska sparas till. |
| [get_IsExportNeeded](./get_isexportneeded/)() const | Tillåter att ange om det aktuella teckensnittet ska exporteras som en teckensnittresurs. Standard är **true**. |
| [get_IsSubsettingNeeded](./get_issubsettingneeded/)() const | Tillåter att ange om det aktuella teckensnittet ska delmängdas innan export som en teckensnittresurs. |
| [get_Italic](./get_italic/)() const | Indikerar om det aktuella teckensnittet är kursivt. |
| [get_KeepFontStreamOpen](./get_keepfontstreamopen/)() const | Anger om Aspose.Words ska hålla strömmen öppen eller stänga den efter att ett teckensnitt har sparats. |
| [get_OriginalFileName](./get_originalfilename/)() const | Hämtar det ursprungliga teckensnittsfilnamnet med filändelse. |
| [get_OriginalFileSize](./get_originalfilesize/)() const | Hämtar den ursprungliga teckensnittsfilens storlek. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FontFileName](./set_fontfilename/)(const System::String\&) | Sättare för [Aspose::Words::Saving::FontSavingArgs::get_FontFileName](./get_fontfilename/). |
| [set_FontStream](./set_fontstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Sättare för [Aspose::Words::Saving::FontSavingArgs::get_FontStream](./get_fontstream/). |
| [set_FontStream](./set_fontstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | Tillåter att ange om det aktuella teckensnittet ska exporteras som en teckensnittresurs. Standard är **true**. |
| [set_IsSubsettingNeeded](./set_issubsettingneeded/)(bool) | Sättare för [Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded](./get_issubsettingneeded/). |
| [set_KeepFontStreamOpen](./set_keepfontstreamopen/)(bool) | Sättare för [Aspose::Words::Saving::FontSavingArgs::get_KeepFontStreamOpen](./get_keepfontstreamopen/). |
| static [Type](./type/)() |  |
## Anmärkningar


När Aspose.Words sparar ett dokument till HTML eller relaterade format och [ExportFontResources](../htmlsaveoptions/get_exportfontresources/) är satt till **true**, sparas varje teckensnitt som ska exporteras i en separat fil.

[FontSavingArgs](./) controls whether particular font resource should be exported and how.

[FontSavingArgs](./) also allows to redefine how font file names are generated or to completely circumvent saving of fonts into files by providing your own stream objects.

För att avgöra om en viss teckensnittresurs ska sparas, använd egenskapen [IsExportNeeded](./get_isexportneeded/).

För att spara teckensnitt i strömmar istället för filer, använd egenskapen [FontStream](./get_fontstream/).
## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
