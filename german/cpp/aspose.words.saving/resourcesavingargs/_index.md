---
title: "Aspose::Words::Saving::ResourceSavingArgs Klasse"
linktitle: "ResourceSavingArgs"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ResourceSavingArgs Klasse. Stellt Daten für das ResourceSaving()-Ereignis bereit. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 27000
url: /de/cpp/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class


Stellt Daten für das [ResourceSaving()](../iresourcesavingcallback/resourcesaving/) Ereignis bereit. Weitere Informationen finden Sie im [Dokument speichern](https://docs.aspose.com/words/cpp/save-a-document/) Dokumentationsartikel.

```cpp
class ResourceSavingArgs : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Document](./get_document/)() const | Liefert das Dokumentobjekt, das gerade gespeichert wird. |
| [get_KeepResourceStreamOpen](./get_keepresourcestreamopen/)() const | Gibt an, ob Aspose.Words den Stream offen halten oder nach dem Speichern einer Ressource schließen soll. |
| [get_ResourceFileName](./get_resourcefilename/)() const | Liest oder setzt den Dateinamen (ohne Pfad), in dem die Ressource gespeichert wird. |
| [get_ResourceFileUri](./get_resourcefileuri/)() const | Liest oder setzt den Uniform Resource Identifier (URI), der verwendet wird, um die Ressourcendatei aus dem Dokument zu referenzieren. |
| [get_ResourceStream](./get_resourcestream/)() const | Ermöglicht die Angabe des Streams, in dem die Ressource gespeichert wird. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_KeepResourceStreamOpen](./set_keepresourcestreamopen/)(bool) | Setter für [Aspose::Words::Saving::ResourceSavingArgs::get_KeepResourceStreamOpen](./get_keepresourcestreamopen/). |
| [set_ResourceFileName](./set_resourcefilename/)(const System::String\&) | Setter für [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName](./get_resourcefilename/). |
| [set_ResourceFileUri](./set_resourcefileuri/)(const System::String\&) | Setter für [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri](./get_resourcefileuri/). |
| [set_ResourceStream](./set_resourcestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Setter für [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream](./get_resourcestream/). |
| [set_ResourceStream](./set_resourcestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |
## Hinweise


Standardmäßig speichert Aspose.Words ein Dokument als feste Seiten‑HTML, SVG oder Markdown, indem es jede Ressource in einer separaten Datei ablegt. Aspose.Words verwendet den Dokumentdateinamen und eine eindeutige Nummer, um für jede im Dokument gefundene Ressource einen eindeutigen Dateinamen zu erzeugen.

[ResourceSavingArgs](./) allows to redefine how resource file names are generated or to completely circumvent saving of resources into files by providing your own stream objects.

Um Ihre eigene Logik zur Generierung von Ressourcendateinamen anzuwenden, verwenden Sie die Eigenschaft [ResourceFileName](./get_resourcefilename/).

Um Ressourcen in Streams statt in Dateien zu speichern, verwenden Sie die Eigenschaft [ResourceStream](./get_resourcestream/).
## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
