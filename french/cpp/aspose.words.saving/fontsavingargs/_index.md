---
title: "Aspose::Words::Saving::FontSavingArgs class"
linktitle: "FontSavingArgs"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::FontSavingArgs class. Fournit des données pour l'événement FontSaving(). Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class


Fournit des données pour l'événement [FontSaving()](../ifontsavingcallback/fontsaving/). Pour en savoir plus, consultez l'article de documentation [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class FontSavingArgs : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Bold](./get_bold/)() const | Indique si la police actuelle est en gras. |
| [get_Document](./get_document/)() const | Obtient l'objet document qui est en cours d'enregistrement. |
| [get_FontFamilyName](./get_fontfamilyname/)() const | Indique le nom de la famille de police actuelle. |
| [get_FontFileName](./get_fontfilename/)() const | Obtient ou définit le nom de fichier (sans le chemin) où la police sera enregistrée. |
| [get_FontStream](./get_fontstream/)() const | Permet de spécifier le flux où la police sera enregistrée. |
| [get_IsExportNeeded](./get_isexportneeded/)() const | Permet de spécifier si la police actuelle sera exportée en tant que ressource de police. La valeur par défaut est **true**. |
| [get_IsSubsettingNeeded](./get_issubsettingneeded/)() const | Permet de spécifier si la police actuelle sera sous‑ensemble avant d'être exportée en tant que ressource de police. |
| [get_Italic](./get_italic/)() const | Indique si la police actuelle est en italique. |
| [get_KeepFontStreamOpen](./get_keepfontstreamopen/)() const | Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après avoir enregistré une police. |
| [get_OriginalFileName](./get_originalfilename/)() const | Obtient le nom de fichier de police original avec son extension. |
| [get_OriginalFileSize](./get_originalfilesize/)() const | Obtient la taille du fichier de police original. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FontFileName](./set_fontfilename/)(const System::String\&) | Définisseur pour [Aspose::Words::Saving::FontSavingArgs::get_FontFileName](./get_fontfilename/). |
| [set_FontStream](./set_fontstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Définisseur pour [Aspose::Words::Saving::FontSavingArgs::get_FontStream](./get_fontstream/). |
| [set_FontStream](./set_fontstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | Permet de spécifier si la police actuelle sera exportée en tant que ressource de police. La valeur par défaut est **true**. |
| [set_IsSubsettingNeeded](./set_issubsettingneeded/)(bool) | Définisseur pour [Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded](./get_issubsettingneeded/). |
| [set_KeepFontStreamOpen](./set_keepfontstreamopen/)(bool) | Définisseur pour [Aspose::Words::Saving::FontSavingArgs::get_KeepFontStreamOpen](./get_keepfontstreamopen/). |
| static [Type](./type/)() |  |
## Remarques


Lorsque Aspose.Words enregistre un document au format HTML ou formats associés et que [ExportFontResources](../htmlsaveoptions/get_exportfontresources/) est défini sur **true**, il enregistre chaque police concernée pour l'exportation dans un fichier séparé.

[FontSavingArgs](./) controls whether particular font resource should be exported and how.

[FontSavingArgs](./) also allows to redefine how font file names are generated or to completely circumvent saving of fonts into files by providing your own stream objects.

Pour décider s'il faut enregistrer une ressource de police particulière, utilisez la propriété [IsExportNeeded](./get_isexportneeded/).

Pour enregistrer les polices dans des flux au lieu de fichiers, utilisez la propriété [FontStream](./get_fontstream/).
## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
