---
title: "Aspose::Words::Saving::FontSavingArgs class"
linktitle: "FontSavingArgs"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::FontSavingArgs Klasse. Stellt Daten für das FontSaving()-Ereignis bereit. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class


Stellt Daten für das [FontSaving()](../ifontsavingcallback/fontsaving/) Ereignis bereit. Weitere Informationen finden Sie im Dokumentationsartikel [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class FontSavingArgs : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Bold](./get_bold/)() const | Gibt an, ob die aktuelle Schriftart fett ist. |
| [get_Document](./get_document/)() const | Liefert das Dokumentobjekt, das gespeichert wird. |
| [get_FontFamilyName](./get_fontfamilyname/)() const | Gibt den Namen der aktuellen Schriftfamilie an. |
| [get_FontFileName](./get_fontfilename/)() const | Liest oder setzt den Dateinamen (ohne Pfad), in dem die Schriftart gespeichert wird. |
| [get_FontStream](./get_fontstream/)() const | Ermöglicht die Angabe des Streams, in dem die Schriftart gespeichert wird. |
| [get_IsExportNeeded](./get_isexportneeded/)() const | Ermöglicht die Angabe, ob die aktuelle Schriftart als Schriftressource exportiert werden soll. Standardwert ist **true**. |
| [get_IsSubsettingNeeded](./get_issubsettingneeded/)() const | Ermöglicht die Angabe, ob die aktuelle Schriftart vor dem Export als Schriftressource teilunterteilt werden soll. |
| [get_Italic](./get_italic/)() const | Gibt an, ob die aktuelle Schriftart kursiv ist. |
| [get_KeepFontStreamOpen](./get_keepfontstreamopen/)() const | Gibt an, ob Aspose.Words den Stream nach dem Speichern einer Schriftart offen halten oder schließen soll. |
| [get_OriginalFileName](./get_originalfilename/)() const | Liefert den ursprünglichen Schriftdateinamen mit Erweiterung. |
| [get_OriginalFileSize](./get_originalfilesize/)() const | Liefert die ursprüngliche Schriftdateigröße. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FontFileName](./set_fontfilename/)(const System::String\&) | Setter für [Aspose::Words::Saving::FontSavingArgs::get_FontFileName](./get_fontfilename/). |
| [set_FontStream](./set_fontstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Setter für [Aspose::Words::Saving::FontSavingArgs::get_FontStream](./get_fontstream/). |
| [set_FontStream](./set_fontstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | Ermöglicht die Angabe, ob die aktuelle Schriftart als Schriftressource exportiert werden soll. Standardwert ist **true**. |
| [set_IsSubsettingNeeded](./set_issubsettingneeded/)(bool) | Setter für [Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded](./get_issubsettingneeded/). |
| [set_KeepFontStreamOpen](./set_keepfontstreamopen/)(bool) | Setter für [Aspose::Words::Saving::FontSavingArgs::get_KeepFontStreamOpen](./get_keepfontstreamopen/). |
| static [Type](./type/)() |  |
## Hinweise


Wenn Aspose.Words ein Dokument in HTML oder verwandte Formate speichert und [ExportFontResources](../htmlsaveoptions/get_exportfontresources/) auf **true** gesetzt ist, wird jede Schriftart für den Export in einer separaten Datei gespeichert.

[FontSavingArgs](./) controls whether particular font resource should be exported and how.

[FontSavingArgs](./) also allows to redefine how font file names are generated or to completely circumvent saving of fonts into files by providing your own stream objects.

Um zu entscheiden, ob eine bestimmte Schriftressource gespeichert werden soll, verwenden Sie die Eigenschaft [IsExportNeeded](./get_isexportneeded/).

Um Schriftarten in Streams statt in Dateien zu speichern, verwenden Sie die Eigenschaft [FontStream](./get_fontstream/).
## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
