---
title: "Aspose::Words::Saving::CssSavingArgs Klasse"
linktitle: "CssSavingArgs"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::CssSavingArgs Klasse. Stellt Daten für das CssSaving()-Ereignis bereit. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class


Stellt Daten für das [CssSaving()](../icsssavingcallback/csssaving/) Ereignis bereit. Weitere Informationen finden Sie im [Dokument speichern](https://docs.aspose.com/words/cpp/save-a-document/) Dokumentationsartikel.

```cpp
class CssSavingArgs : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_CssStream](./get_cssstream/)() const | Ermöglicht das Angeben des Streams, in dem die CSS-Informationen gespeichert werden. |
| [get_Document](./get_document/)() const | Liefert das Dokumentobjekt, das gerade gespeichert wird. |
| [get_IsExportNeeded](./get_isexportneeded/)() const | Ermöglicht das Angeben, ob das CSS in eine Datei exportiert und in das HTML-Dokument eingebettet wird. Standardwert ist **true**. Wenn diese Eigenschaft **false** ist, werden die CSS-Informationen nicht in einer CSS-Datei gespeichert und nicht in das HTML-Dokument eingebettet. |
| [get_KeepCssStreamOpen](./get_keepcssstreamopen/)() const | Gibt an, ob Aspose.Words den Stream nach dem Speichern von CSS-Informationen offen halten oder schließen soll. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CssStream](./set_cssstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Setter für [Aspose::Words::Saving::CssSavingArgs::get_CssStream](./get_cssstream/). |
| [set_CssStream](./set_cssstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | Ermöglicht das Angeben, ob das CSS in eine Datei exportiert und in das HTML-Dokument eingebettet wird. Standardwert ist **true**. Wenn diese Eigenschaft **false** ist, werden die CSS-Informationen nicht in einer CSS-Datei gespeichert und nicht in das HTML-Dokument eingebettet. |
| [set_KeepCssStreamOpen](./set_keepcssstreamopen/)(bool) | Setter für [Aspose::Words::Saving::CssSavingArgs::get_KeepCssStreamOpen](./get_keepcssstreamopen/). |
| static [Type](./type/)() |  |
## Hinweise


Standardmäßig speichert Aspose.Words beim Speichern eines Dokuments als HTML die CSS-Informationen inline (als Wert des **style**-Attributs jedes Elements).

[CssSavingArgs](./) allows to save CSS information into file by providing your own stream object.

Um CSS in einen Stream zu speichern, verwenden Sie die Eigenschaft [CssStream](./get_cssstream/).

Um das Speichern von CSS in eine Datei und das Einbetten in das HTML-Dokument zu unterdrücken, verwenden Sie die Eigenschaft [IsExportNeeded](./get_isexportneeded/).
## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
