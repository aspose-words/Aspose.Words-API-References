---
title: "Aspose::Words::Saving::FontSavingArgs class"
linktitle: "FontSavingArgs"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::FontSavingArgs class. Fornisce dati per l'evento FontSaving(). Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class


Fornisce dati per l'evento [FontSaving()](../ifontsavingcallback/fontsaving/). Per saperne di più, visita l'articolo di documentazione [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class FontSavingArgs : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Bold](./get_bold/)() const | Indica se il carattere corrente è in grassetto. |
| [get_Document](./get_document/)() const | Ottiene l'oggetto documento che viene salvato. |
| [get_FontFamilyName](./get_fontfamilyname/)() const | Indica il nome della famiglia di caratteri corrente. |
| [get_FontFileName](./get_fontfilename/)() const | Ottiene o imposta il nome del file (senza percorso) dove il carattere verrà salvato. |
| [get_FontStream](./get_fontstream/)() const | Consente di specificare lo stream dove il carattere verrà salvato. |
| [get_IsExportNeeded](./get_isexportneeded/)() const | Consente di specificare se il carattere corrente verrà esportato come risorsa di carattere. Il valore predefinito è **true**. |
| [get_IsSubsettingNeeded](./get_issubsettingneeded/)() const | Consente di specificare se il carattere corrente sarà ridotto a sottoinsieme prima di essere esportato come risorsa di carattere. |
| [get_Italic](./get_italic/)() const | Indica se il carattere corrente è in corsivo. |
| [get_KeepFontStreamOpen](./get_keepfontstreamopen/)() const | Specifica se Aspose.Words deve mantenere il flusso aperto o chiuderlo dopo aver salvato un carattere. |
| [get_OriginalFileName](./get_originalfilename/)() const | Ottiene il nome originale del file del carattere con estensione. |
| [get_OriginalFileSize](./get_originalfilesize/)() const | Ottiene la dimensione originale del file del carattere. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FontFileName](./set_fontfilename/)(const System::String\&) | Impostatore per [Aspose::Words::Saving::FontSavingArgs::get_FontFileName](./get_fontfilename/). |
| [set_FontStream](./set_fontstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Impostatore per [Aspose::Words::Saving::FontSavingArgs::get_FontStream](./get_fontstream/). |
| [set_FontStream](./set_fontstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | Consente di specificare se il carattere corrente verrà esportato come risorsa di carattere. Il valore predefinito è **true**. |
| [set_IsSubsettingNeeded](./set_issubsettingneeded/)(bool) | Impostatore per [Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded](./get_issubsettingneeded/). |
| [set_KeepFontStreamOpen](./set_keepfontstreamopen/)(bool) | Impostatore per [Aspose::Words::Saving::FontSavingArgs::get_KeepFontStreamOpen](./get_keepfontstreamopen/). |
| static [Type](./type/)() |  |
## Note


Quando Aspose.Words salva un documento in HTML o formati correlati e [ExportFontResources](../htmlsaveoptions/get_exportfontresources/) è impostato su **true**, salva ogni carattere soggetto all'esportazione in un file separato.

[FontSavingArgs](./) controls whether particular font resource should be exported and how.

[FontSavingArgs](./) also allows to redefine how font file names are generated or to completely circumvent saving of fonts into files by providing your own stream objects.

Per decidere se salvare una risorsa di carattere specifica, usa la proprietà [IsExportNeeded](./get_isexportneeded/).

Per salvare i caratteri in flussi anziché in file, usa la proprietà [FontStream](./get_fontstream/).
## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
