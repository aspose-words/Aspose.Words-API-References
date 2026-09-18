---
title: "Aspose::Words::Saving::DocumentPartSavingArgs Klasse"
linktitle: "DocumentPartSavingArgs"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::DocumentPartSavingArgs Klasse. Stellt Daten für den DocumentPartSaving()-Callback bereit. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.saving/documentpartsavingargs/
---
## DocumentPartSavingArgs class


Stellt Daten für den [DocumentPartSaving()](../idocumentpartsavingcallback/documentpartsaving/) Callback bereit. Weitere Informationen finden Sie im Artikel [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/) der Dokumentation.

```cpp
class DocumentPartSavingArgs : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Document](./get_document/)() const | Liefert das Dokumentobjekt, das gespeichert wird. |
| [get_DocumentPartFileName](./get_documentpartfilename/)() const | Liest oder setzt den Dateinamen (ohne Pfad), in dem der Dokumentteil gespeichert wird. |
| [get_DocumentPartStream](./get_documentpartstream/)() const | Ermöglicht die Angabe des Streams, in dem der Dokumentteil gespeichert wird. |
| [get_KeepDocumentPartStreamOpen](./get_keepdocumentpartstreamopen/)() const | Gibt an, ob Aspose.Words den Stream nach dem Speichern eines Dokumentteils offen halten oder schließen soll. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DocumentPartFileName](./set_documentpartfilename/)(const System::String\&) | Setter für [Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName](./get_documentpartfilename/). |
| [set_DocumentPartStream](./set_documentpartstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Setter für [Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream](./get_documentpartstream/). |
| [set_DocumentPartStream](./set_documentpartstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_KeepDocumentPartStreamOpen](./set_keepdocumentpartstreamopen/)(bool) | Setter für [Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen](./get_keepdocumentpartstreamopen/). |
| static [Type](./type/)() |  |
## Hinweise


Wenn Aspose.Words ein Dokument als HTML oder in verwandten Formaten speichert und [DocumentSplitCriteria](../htmlsaveoptions/get_documentsplitcriteria/) angegeben ist, wird das Dokument in Teile aufgeteilt und standardmäßig wird jeder Dokumentteil in einer separaten Datei gespeichert.

Die Klasse [DocumentPartSavingArgs](./) ermöglicht es Ihnen, zu steuern, wie jeder Dokumentteil gespeichert wird. Sie erlaubt, die Erzeugung von Dateinamen neu zu definieren oder das Speichern von Dokumentteilen in Dateien vollständig zu umgehen, indem Sie eigene Stream‑Objekte bereitstellen.

Um Dokumentteile in Streams statt in Dateien zu speichern, verwenden Sie die Eigenschaft [DocumentPartStream](./get_documentpartstream/).
## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
